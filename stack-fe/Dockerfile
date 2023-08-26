# Stage 1
FROM node:16-alpine as build-stage
WORKDIR /usr/frontend
COPY . .
# Stage 2
FROM nginx:1.23.3
COPY --from=build-stage /usr/frontend /usr/share/nginx/html
CMD nginx -g "daemon off;"
