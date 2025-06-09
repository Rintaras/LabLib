# LabLib

## 使用技術
- Vite (React + TypeScript)
- Docker, Docker Compose
- Node.js

## Dockerを使用した開発環境のセットアップ

### 前提条件
- Docker
- Docker Compose

### 起動方法
1. リポジトリをクローン
```bash
git clone [リポジトリURL]
cd LabLib
```

2. Dockerコンテナのビルドと起動
```bash
docker-compose up --build
```

3. アプリケーションにアクセス
ブラウザで http://localhost:3000 にアクセス

### コンテナの停止
```bash
docker-compose down
```

### 開発時の注意点
- ホットリロードが有効になっているため、ソースコードの変更は自動的に反映されます
- node_modulesはコンテナ内にマウントされているため、ローカル環境にインストールする必要はありません 

## 開発環境の起動方法

```bash
docker compose up -d --build
```

## 外部アクセスについて

Viteサーバーは`--host`オプションで0.0.0.0バインドされているため、
`http://<サーバーのIP>:5173/` で他のホストからアクセス可能です。

## ポート
- 5173: Vite (React開発サーバー) 