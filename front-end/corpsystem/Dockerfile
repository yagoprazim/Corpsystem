FROM node:18-alpine

WORKDIR /app

COPY .env .env
COPY package.json package-lock.json ./
RUN npm install

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["npx", "serve", "-s", "dist"]
