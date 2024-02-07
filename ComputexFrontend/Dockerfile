FROM node:18-alpine as builder

WORKDIR /reactapp

COPY . /reactapp

RUN npm install

RUN npm run build

#EXPOSE 3000

#CMD ["npm", "run", "start"]

FROM nginx:alpine 

COPY --from=builder /reactapp/dist/ /usr/share/nginx/html