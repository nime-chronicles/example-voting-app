FROM node:8.9-alpine

WORKDIR /app

COPY . .

RUN npm config set registry https://registry.npmjs.org

RUN npm install -g nodemon --unsafe-perm --verbose 

RUN npm install \
 && npm ls \
 && npm cache clean --force \
 && mv /app/node_modules /node_modules

EXPOSE 80

CMD node server.js
