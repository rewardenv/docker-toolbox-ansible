ARG IMAGE_NAME="rewardenv/docker-toolbox"
ARG IMAGE_TAG="debian-buster-slim"
FROM ${IMAGE_NAME}:${IMAGE_TAG}

RUN set -eux \
  && apt-get update && apt-get install -y --no-install-recommends \
     openvpn \
     python3 \
     python3-pip \
     python3-setuptools \
     hcloud-python \
  && pip3 install --upgrade pip \
  && pip3 install --no-cache-dir \
     'ansible<2.11'
RUN echo "nameserver 8.8.8.8" > /etc/resolv.conf