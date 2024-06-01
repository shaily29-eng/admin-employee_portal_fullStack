FROM node:18 as build

WORKDIR /app

COPY package*.json .
RUN yarn && yarn run build

FROM nginx:alpine as production

COPY . .

EXPOSE 3000

CMD [ "npm", "run", "dev" ,"nginx", "-g","daemon off;"]