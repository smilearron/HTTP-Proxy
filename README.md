# HTTP-Proxy

• It creates a TCP server socket to listen for incoming TCP connections on an unused port, and output the host name and port number the proxy is running on.

• When a new connection request comes in, the proxy accepts the connection, establishing a TCP connection with the client.

• The proxy reads HTTP request sent from the client and prepares an HTTP request to send to the HTTP server.

• The proxy starts a new connection with the HTTP server, and sends its prepared HTTP request to the server.

• The proxy reads the HTTP response and forwards the HTTP response (the status line, the response header, and the entity body).

• The proxy closes the TCP connection with the server.

• The proxy sends the server’s response back to the client via its TCP connection with the client. This TCP connection with the client should have remained open during its communication with the server.

• The proxy closes the connection socket to the client.

How to test the programs?
You first download a resource located at a URL using the wget command without the proxy. This is the correct resource. 
Then you download the same resource at the same URL with your proxy. Use the diff command to check if the two downloaded resources matches.

