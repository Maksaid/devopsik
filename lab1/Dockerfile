FROM alpine:latest

RUN apk add --no-cache nginx && \
    mkdir -p /var/www/html && \
    chown -R nginx:nginx /var/www/html && \
    chown -R nginx:nginx /etc/nginx
COPY configuration/nginx.conf /etc/nginx/nginx.conf
USER nginx

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
