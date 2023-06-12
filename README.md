# CST311-TCPClientServer
Team Programming Assignment #3 TCP Client Server

The purpose of this assignment is to develop simple software programs using sockets to achieve communication between two (or more) computers. 
 
The program is written in Python, where the interface to the TCP/IP application programming interface is similar to other C-family programming languages. 

#Client code 
There are two clients, X and Y (both essentially identical) that will communicate with a server. Clients X and Y will each open a TCP socket to the server and wait until the server establishes a connection with both the clients. One of the clients sends a message to the server followed by the other client. The message contains the name of the client followed by a name (e.g., “Client X: Alice”, “Client Y: Bob”).  
Later clients receive a message back from the server, indicating which message arrived at the Server first and which arrived second. The clients should print the message that they sent to the server, followed by the reply received from the server.  
The response message does not rely on the order of the connection establishment. If the connections are established in a different order the response will still be dependent only on the order of the messages received at the server.
 
#Server code 
The server will accept connections from both clients and after it has received messages from both X and Y, the server will print their messages and then send an acknowledgment back to the clients. The acknowledgment from the server should contain the sequence in which the client messages were received (“X: Alice received before Y: Bob”, or “Y: Bob received before X: Alice”). After the server sends out this message it should output a message saying - “Sent acknowledgment to both X and Y”. The server can then terminate.  
The server sits in an infinite loop listening for incoming TCP packets. When a packet comes, the server simply sends it back to the client.
