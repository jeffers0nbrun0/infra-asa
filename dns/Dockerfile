FROM debian:stable
RUN apt-get update -y; apt-get full-update -y; apt autoremove -y
RUN apt-get install bind9 -y; apt-get install utils -y; apt-get install wget -y; apt-get install curl -y 
RUN apt-get install dnsutils apt-get install vim; apt-get install nano; apt-get install bash


# Copiando arquivos de configurações para o container
COPY named.conf.options /etc/bind/
COPY named.conf.local /etc/bind/
COPY db.asa /etc/bind/zones/

CMD ["bin/bash", "-c","while :; do sleep 10;done"]