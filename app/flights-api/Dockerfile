FROM node:10.9.0-alpine

RUN apk upgrade musl

WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci

COPY . .
ENV NODE_ENV "development"
EXPOSE 3003

CMD [ "npm", "run", "container" ]
