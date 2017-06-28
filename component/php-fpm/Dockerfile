FROM phpdockerio/php7-fpm:latest

LABEL version="1.0"
LABEL maintainer="snowcookie@giftpack.io"

RUN apt-get update \
    && echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections \
    && apt-get -y --no-install-recommends -o Dpkg::Options::="--force-confold" install \
       php7.0-common php7.0-mbstring php7.0-dom php7.0-mbstring php7.0-mysql php7.0-redis php7.0-sqlite3 \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

