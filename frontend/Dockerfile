FROM node:9.3.0

RUN mkdir -p /usr/src/app1
WORKDIR /usr/src/app1

COPY package.json /usr/src/app1
RUN npm install

COPY . /usr/src/app1

RUN npm run build
RUN rm -rf ./src


ENV PORT=8081
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

EXPOSE 8081

CMD [ "node", "server.js" ]

USER node
