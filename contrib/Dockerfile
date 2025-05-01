FROM node:18

WORKDIR /app

COPY . .

RUN corepack enable && corepack prepare yarn@stable --activate

RUN yarn install
RUN yarn tsc
RUN yarn build
RUN yarn build:backend

EXPOSE 7007

CMD ["yarn", "start"]
