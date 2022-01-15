FROM golang:1.17-alpine

ENV GO111MODULE=on 

WORKDIR /go/src/github.com/soutaschool/echo-rest/echo-app

COPY go.mod .
COPY go.sum .
RUN go mod download

COPY . .
RUN go build .

RUN go get github.com/pilu/fresh

EXPOSE 8080

CMD ["fresh"]