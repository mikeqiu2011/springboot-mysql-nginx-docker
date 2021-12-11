# nginx-html + springboot application + mysql

## build
docker-compose build

## run
docker-compose up

## test
localhost:30001

## ref
https://www.bezkoder.com/docker-compose-spring-boot-mysql/

## rebuild webserver
docker-compose build webserver && \
docker-compose rm -s -f webserver && \
docker-compose up -d webserver

## rebuild springapp
mvn clean package && \
docker-compose build springapp && \
docker-compose rm -s -f springapp && \
docker-compose up -d springapp