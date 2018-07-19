FROM index.alauda.cn/library/node:5.1-slim

WORKDIR /app

RUN npm install -g nodemon
ADD package.json /app/package.json
RUN npm config set registry http://registry.npmjs.org
RUN npm install && npm ls
RUN mv /app/node_modules /node_modules

ADD . /app

ENV PORT 8080
EXPOSE 8080

CMD ["node", "server.js"]
