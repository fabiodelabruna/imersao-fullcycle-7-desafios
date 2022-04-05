FROM golang:1.18.0-alpine as builder
WORKDIR /build
ADD main.go .
RUN go build -o main main.go

FROM scratch
COPY --from=builder /build/main .
ENTRYPOINT [ "./main" ]
