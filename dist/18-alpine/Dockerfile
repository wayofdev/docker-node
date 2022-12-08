# Auto-generated via Ansible: edit src/Dockerfiles/all/Dockerfile.j2 instead.

FROM node:18-alpine

# Labels
# https://github.com/opencontainers/image-spec/blob/main/annotations.md
LABEL "maintainer"="lotyp <lotyp7@gmail.com>"
LABEL "vendor"="wayofdev"
LABEL "org.opencontainers.image.authors"="lotyp <lotyp7@gmail.com>"
LABEL "org.opencontainers.image.url"="https://hub.docker.com/r/wayofdev/node"
LABEL "org.opencontainers.image.documentation"="https://github.com/wayofdev/docker-node"
LABEL "org.opencontainers.image.source"="https://github.com/wayofdev/docker-node"
LABEL "org.opencontainers.image.vendor"="wayofdev"
LABEL "org.opencontainers.image.licenses"="MIT"
LABEL "org.opencontainers.image.ref.name"="18-alpine"
LABEL "org.opencontainers.image.title"="node-18-alpine"
LABEL "org.opencontainers.image.description"="node-18-alpine"

RUN set -eux; \
  apk add \
    curl \
    git \
  && /bin/ash -c 'set -ex && \
    ARCH=`uname -m` && \
      if [ "$ARCH" == "x86_64" ]; then \
        echo "x86_64" && \
        curl -fsSL "https://github.com/pnpm/pnpm/releases/latest/download/pnpm-linuxstatic-x64" -o /bin/pnpm; \
      elif [ "ARCH" == "arm64" ]; then \
        echo "arm64" && \
        curl -fsSL "https://github.com/pnpm/pnpm/releases/latest/download/pnpm-linuxstatic-arm64" -o /bin/pnpm; \
      else \
         echo "unknown arch" && \
         curl -fsSL "https://github.com/pnpm/pnpm/releases/latest/download/pnpm-linuxstatic-arm64" -o /bin/pnpm; \
      fi' \
  && chmod +x /bin/pnpm
