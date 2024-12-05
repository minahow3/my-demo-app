# ベースイメージとして Node.js の Alpine バージョンを使用
FROM node:18-alpine

# 作業ディレクトリを設定
WORKDIR /app

# package.json と package-lock.json をコピー
COPY package*.json ./

# 依存関係をインストール
RUN npm install

# アプリのソースコードをコピー
COPY . .

# アプリをビルド
RUN npm run build

# 本番用サーバーでビルドを提供
CMD ["npx", "serve", "-s", "build"]