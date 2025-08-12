FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN <<EOF bash
apt-get update
apt-get install -y curl ca-certificates unzip zip tar
apt-get clean
rm -rf /var/lib/apt/lists/*
EOF

USER ubuntu
WORKDIR /home/ubuntu

RUN curl -s "https://get.sdkman.io" | bash

COPY entry.sh /entry.sh

ENTRYPOINT ["/entry.sh"]
