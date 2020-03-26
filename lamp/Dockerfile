FROM ubuntu:18.04

ENV TZ=Europe/Kiev
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update -y
RUN apt install -y apache2

RUN apt install php -y libapache2-mod-php php-mysql

CMD ["apachectl","-D","FOREGROUND"]
RUN a2enmod rewrite

EXPOSE 80
EXPOSE 443

