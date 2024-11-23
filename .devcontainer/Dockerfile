FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

RUN apt-get update && apt-get upgrade -y && \
    apt-get install postgresql -y && \
    apt-get install postgresql-common -y && \
    /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh -y && \
    apt-get install nginx -y && \
    apt-get update -y && sudo apt-get install ufw -y && \
    apt install apache2 -y && \    
    apt-get install php libapache2-mod-php -y && \
    apt-get clean

RUN ufw app list
RUN ufw allow 'Nginx HTTP'
RUN export APACHE_RUN_DIR=/var/run/apache2
RUN export APACHE_LOG_DIR=/var/log/apache2
