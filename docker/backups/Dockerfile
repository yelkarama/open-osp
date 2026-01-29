FROM alpine:3.23.3

RUN apk add --update --no-cache  \
   python \
   lrzip \
   py-pip \
   docker \
  && pip install awscli \ 
  && rm -fr /var/cache/apk/*

COPY ./backups.sh /backups.sh
COPY ./startup.sh /startup.sh

RUN chmod +x /backups.sh
RUN chmod +x /startup.sh