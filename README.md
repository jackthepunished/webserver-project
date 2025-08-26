# A TCP C Web Server

A very simple web server written in C.

## Build and Run

```sh
gcc server.c -o server
./server
```

## Development Steps

1.  **Setup**: Created `server.c` and a simple `index.html`.
2.  **Includes & Constants**: Added standard C libraries and defined `PORT` and `BUFFER_SIZE`.
3.  **TCP Socket**: Created a new TCP socket using `socket()`.
4.  **Easy Restarts**: Used `setsockopt()` with `SO_REUSEADDR` to allow the address to be reused immediately after the server is stopped.
5.  **Bind**: Bound the socket to `0.0.0.0:8080` using `bind()`.
6.  **Listen**: Started listening for incoming connections with `listen()`.
7.  **Accept Loop**: Created an infinite loop to `accept()` new client connections.
8.  **HTTP Response**: Implemented helper functions to send a basic `HTTP/1.1 200 OK` header and the content of a file.
9.  **Integration**: Called the helper functions from the main loop to serve `index.html` to connected clients.
10. **Build & Run**: Compiled the server code with `gcc` and ran the resulting executable.
