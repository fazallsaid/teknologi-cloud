FROM smebberson/alpine-base:3.0.0
MAINTAINER  Muhammad Agung Nugroho <nugroho.agung.m@gmail.com>

# Install nginx
RUN echo "http://dl-4.alpinelinux.org/alpine/v3.3/main" >> /etc/apk/repositories && \
    apk add --update nginx=1.8.1-r1 && \
    rm -rf /var/cache/apk/* && \
    chown -R nginx:www-data /var/lib/nginx

# Expose TCP port untuk nginx
EXPOSE 80 443

# Menjalankan NGINX Webserver
CMD ["nginx", "-g", "daemon off;"]
