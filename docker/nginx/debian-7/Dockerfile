#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/nginx:debian-7
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/base:debian-7

MAINTAINER info@webdevops.io
LABEL vendor=WebDevOps.io
LABEL io.webdevops.layout=8
LABEL io.webdevops.version=0.55.1

ENV WEB_DOCUMENT_ROOT  /app
ENV WEB_DOCUMENT_INDEX index.php
ENV WEB_ALIAS_DOMAIN   *.vm

COPY conf/ /opt/docker/

# Install nginx
RUN /usr/local/bin/apt-install \
        nginx \
    && /opt/docker/bin/provision run --tag bootstrap --role webdevops-nginx \
    && /opt/docker/bin/bootstrap.sh


EXPOSE 80 443
