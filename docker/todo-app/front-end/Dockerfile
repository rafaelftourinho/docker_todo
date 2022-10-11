FROM node:14-alpine AS build

WORKDIR /app

EXPOSE 3000

COPY ["package.json", "package-lock.json", "./"]
RUN npm install

COPY . .
ADD ["node_modules.tar.gz", "./"]

RUN npm run build

ENTRYPOINT ["npm", "start"]
