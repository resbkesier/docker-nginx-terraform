FROM ubuntu:16.04
MAINTAINER "renato.silva@rocketmail.com"


RUN apt-get update  -y \
    && apt-get install -y nginx \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* var/tmp/* \
    && echo "daemon off;" >> /etc/nginx/nginx.conf

ADD default /etc/nginx/sistes-available/default
ADD index.html /var/www/html/index.html

EXPOSE 80

CMD ["nginx"]
