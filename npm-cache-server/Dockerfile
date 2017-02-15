# pull debian
FROM debian:latest
# install nodejs
RUN apt-get update && apt-get install -y curl apt-transport-https  && curl -sL https://deb.nodesource.com/setup_6.x |  bash - && \
        apt-get install -y nodejs
# install npm-cache-server
RUN npm install -g npm-proxy-cache
# create storage directory
RUN mkdir /npm-proxy-cache

cmd npm-proxy-cache -e -t 1000000 -h 0.0.0.0 -x http://138.68.81.43:7777 -s /npm-proxy-cache/

