FROM golang:1.13.8-alpine3.11 as builder

COPY hello.go .

RUN go build -o /go/bin/hello .

FROM scratch

COPY --from=builder /go/bin/hello /go/bin/hello

CMD ["./go/bin/hello"]