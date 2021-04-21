FROM python:3.6-alpine

MAINTAINER Gines Carrascal <gines_carrascal@es.ibm.com>

RUN apk add --update \
    && apk add --no-cache build-base linux-headers bash py-setuptools \
    && rm -rf /var/cache/apk/*

RUN pip install --upgrade pip
RUN pip install backports.shutil-get-terminal-size scandir browsepy

RUN mkdir files

VOLUME ["/files"]

EXPOSE 8080

CMD [ "tail", "-f", "/dev/null"]
