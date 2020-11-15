FROM registry.access.redhat.com/ubi7/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/example-k8s-operator-golang \
    USER_UID=1001 \
    USER_NAME=example-k8s-operator-golang

# install operator binary
COPY build/_output/bin/example-k8s-operator-golang ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
