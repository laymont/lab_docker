# Usa la imagen oficial de PHP con Nginx
FROM php:8.3-fpm

# Instala extensiones de PHP
RUN apt-get update && \
    apt-get install -y nginx libnginx-mod-http-passenger && \
    docker-php-ext-install pdo pdo_mysql

# Copia la configuración de Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Exponer el puerto 80
EXPOSE 8081

# Comando para iniciar Nginx y PHP-FPM
CMD service nginx start && php-fpm-b"