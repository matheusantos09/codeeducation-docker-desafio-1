FROM golang:alpine AS build

WORKDIR /src/

ENV GO111MODULE=auto

COPY main.go go.* /src/

RUN CGO_ENABLED=0 go build -o /bin/desafio1

FROM scratch
COPY --from=build /bin/desafio1 /bin/desafio1
ENTRYPOINT ["/bin/desafio1"]