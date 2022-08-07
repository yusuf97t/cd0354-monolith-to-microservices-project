FROM beevelop/ionic:latest AS ionic
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm ci
COPY . .
RUN ionic build
FROM nginx:alpine
COPY --from=ionic /urs/src/app/www/usr/share/nginx/html