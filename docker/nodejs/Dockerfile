FROM node:16

WORKDIR /var/www/app
RUN mkdir node_modules

COPY package*.json ./

RUN chown -R node:node /var/www
RUN usermod -u 1000 node

EXPOSE 3000 
CMD yarn --frozen-lockfile && \
    yarn add -dev webpack-dev-server && \
    yarn dev
