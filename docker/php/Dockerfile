FROM php:8.2-fpm-bullseye
# install composer
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -f -n -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
vim
RUN apt-get update \
  && apt-get install -y libpq-dev \
  && docker-php-ext-install pdo_pgsql pdo_mysql
WORKDIR /var/www/html
