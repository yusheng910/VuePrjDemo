# 使用 node 來 serve 靜態檔案（用 serve 套件）
FROM node:18-alpine

WORKDIR /app

# 安裝依賴與建置
COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# 安裝靜態伺服器
RUN npm install -g serve

# 使用 serve 啟動打包後的內容
CMD ["serve", "-s", "dist", "-l", "5173"]

EXPOSE 5173
