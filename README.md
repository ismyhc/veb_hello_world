### Veb Hello World

![V Language](https://img.shields.io/badge/language-V-blue.svg)

This is a simple web application that displays "Hello, World!" in a web browser. It is written using vlang's [veb](https://modules.vlang.io/veb.html) framework. This was created as a learning exercise to peform a benchmark using wrk command line tool.

### How to run the application
`v . -prod` to compile the application and run the executable.
`./veb_hello_world` to run the executable.

### Benchmarking
`wrk -t16 -c400 -d15s http://localhost:8080/` to perform a benchmark test.

### Results I got on my macbook pro m1 max
```
❯ wrk -t16 -c400 -d15s http://localhost:8080
Running 15s test @ http://localhost:8080
  16 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     8.94ms   25.16ms 724.32ms   99.34%
    Req/Sec     3.45k   809.78    31.43k    99.42%
  825481 requests in 15.10s, 71.64MB read
  Socket errors: connect 0, read 397, write 0, timeout 0
Requests/sec:  54653.88
Transfer/sec:      4.74MB
```