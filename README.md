# simple proxy

It's a proxy server. Just forwarding data from client to server with saving logs.
My server isn't multithreaded, for tracking events(connect, ready for reading) i'm using poll.

1) make
2) ./proxy 8080 127.0.0.1 6667 (./proxy listening port, ip address of server to forward, port server to forward)

logs are in directory "log"

example to connect with web server:
1) ./proxy 8080 142.250.145.93 80 (youtube's ip is 142.250.145.93, port is 80)
2) open next console write: "nc 127.0.0.1 8080" to connect with proxy, then write something, youtube will answer and send html file (we don't parse it, but can receive)
3) proxy works
