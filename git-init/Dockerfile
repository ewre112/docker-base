FROM --platform=$TARGETPLATFORM yolean/builder-base

COPY git-init-tekton-compatible.sh /usr/local/bin/

ENTRYPOINT [ "git-init-tekton-compatible.sh" ]

ENV \
  GIT_HTTP_LOW_SPEED_LIMIT=1000 \
  GIT_HTTP_LOW_SPEED_TIME=60

RUN set -ex; \
  git config --global init.defaultBranch main; \
  git config --global advice.detachedHead false; \
  true
