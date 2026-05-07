FROM mcr.microsoft.com/devcontainers/base:ubuntu

RUN apt-get update && apt-get install -y \
    wget \
    tar \
    python3 \
    python3-pip \
    git \
    gcc \
    gdb \
    make \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /opt

RUN wget https://builds.renode.io/renode-latest.linux-portable.tar.gz && \
    tar -xzf renode-latest.linux-portable.tar.gz && \
    mv renode_* renode

ENV PATH="/opt/renode:${PATH}"
