FROM       golang:1.15.7
WORKDIR    /registry
COPY       go.mod .
COPY       go.sum .
RUN        go mod download
COPY       . .
RUN        go build -o registry ./cmd/main.go
ENTRYPOINT ["./registry"]
