# CREATION-FOR-CHAT-USING-TCP-SOCKETS
CREATION FOR CHAT USING TCP SOCKETS

EXP: 6

DATE:

AIM:

To write a python program for creating Chat using TCP Sockets Links.

ALGORITHM:

1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program


PROGRAM:

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```

OUTPUT:

CLIENT:

![6client](https://github.com/MaheshMuthuL/CREATION-FOR-CHAT-USING-TCP-SOCKETS/assets/135570619/aaac8d82-765c-434a-b873-833a20d6fade)








SERVER:

![6server](https://github.com/MaheshMuthuL/CREATION-FOR-CHAT-USING-TCP-SOCKETS/assets/135570619/05c7629a-2407-441e-b734-4d63a46d37d7)






RESULT:

Thus, the python program for creating Chat using TCP Sockets Links was successfully
created and executed.
