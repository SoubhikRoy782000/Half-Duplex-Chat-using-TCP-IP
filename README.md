# Half-Duplex-Chat-using-TCP-IP

Aim -

A half duplex application, where the Client establishes a connection with the Server. The Client can send and the server well receive messages at the same time and then they exchange messages in half duplex manner.


Algorithm -

1. Create a TCP server socket.

2. Bind the socket to a server address.23

3. Start a client socket while the server socket is passive and waiting for the client to connect.

4. Once connection is established, one message can be transferred from the server socket while the client socket waits to receive it.

5. Once the client socket receives the message, it can publish a message to the server socket while the server socket waits passively.

Server:

Step 1: Socket creation: int sockfd = socket(domain, type, protocol)

Step 2: Setsockopt: int setsockopt(int sockfd, int level, int optname, const void *optval, socklen_t optlen);

Step 3: Bind: int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);

Step 4: Listen: int listen(int sockfd, int backlog);

Step 5: Accept: int new_socket= accept(int sockfd, struct sockaddr *addr, socklen_t *addrlen);

Client:

Step 1: Socket creation: int sockfd = socket(domain, type, protocol)

Step 2: Setsockopt: int setsockopt(int sockfd, int level, int optname, const void *optval, socklen_t optlen);

Step 3: Bind: int bind(int sockfd, const struct sockaddr *addr, socklen_t addrlen);

Step 4: Listen: int listen(int sockfd, int backlog);

Step 5: Accept: int new_socket= accept(int sockfd, struct sockaddr *addr, socklen_t *addrlen);

Step 6: Connect: int connect(int sockfd, const struct sockaddr *addr, socklen_t addrlen);


To execute the program use command python3 program_filename.py in terminal where the path is set to the location of the file.
