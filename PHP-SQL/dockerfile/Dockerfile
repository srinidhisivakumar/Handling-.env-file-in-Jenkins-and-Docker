FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -yq --no-install-recommends \
    apache2 \
    libapache2-mod-php7.2 \
    php7.2-mysql \
    mysql-client \
    && rm -rf /var/lib/apt/lists/*
COPY ./app /var/www/html
CMD apachectl -D FOREGROUND
