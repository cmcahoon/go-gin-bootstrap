# go-gin-bootstrap

Clone this repository to have a Go + Gin server up and running in no time!

[Go](https://github.com/golang/go) is an open source programming language that makes it easy to build simple, reliable, and efficient software.

[Gin](https://gin-gonic.com/) is the fastest full-featured web framework for Go.

## Tool Versions

| Tool | Version | Notes |
|---|---|---|
| Go | 1.11+ | This project is based on [go modules](https://github.com/golang/go/wiki/Modules). |
| Gin | 1.3.0 | |

## Usage

### Compile and Run

From the project root:
```bash
# OPTION 1: Compile and Run
#
$ go build
$ ./go-gin-bootstrap
[GIN-debug] [WARNING] Now Gin requires Go 1.6 or later and Go 1.7 will be required soon.

[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /ping                     --> main.main.func1 (3 handlers)
[GIN-debug] Environment variable PORT is undefined. Using port :8080 by default
[GIN-debug] Listening and serving HTTP on :8080


# OPTION 2: Run Directly
#
$ go run example.go
[GIN-debug] [WARNING] Now Gin requires Go 1.6 or later and Go 1.7 will be required soon.

[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /ping                     --> main.main.func1 (3 handlers)
[GIN-debug] Environment variable PORT is undefined. Using port :8080 by default
[GIN-debug] Listening and serving HTTP on :8080
```

To test the server:

```bash
$ curl -v localhost:8080/ping
*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
> GET /ping HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.64.1
> Accept: */*
> 
< HTTP/1.1 200 OK
< Content-Type: application/json; charset=utf-8
< Date: Sat, 20 Apr 2019 17:27:07 GMT
< Content-Length: 18
< 
* Connection #0 to host localhost left intact
{"message":"pong"}* Closing connection 0
```