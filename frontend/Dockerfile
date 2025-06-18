FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm install
RUN npm install axios bootstrap

COPY . .

RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "dist", "-l", "3000"]
