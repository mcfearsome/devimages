ARG VERSION=1.15
FROM golang:$VERSION-buster

WORKDIR /usr/src/app

# setup okteto message
COPY okteto-go/bashrc /root/.bashrc

RUN apt update
RUN apt install build-essential

RUN go get github.com/codegangsta/gin && \
    go get -u github.com/go-delve/delve/cmd/dlv && \
    go get -u golang.org/x/tools/gopls

CMD ["bash"]