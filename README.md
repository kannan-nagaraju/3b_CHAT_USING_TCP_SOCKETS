# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## Server:;
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
## OUPUT:
## Client:
![image](https://github.com/kannan-nagaraju/3b_CHAT_USING_TCP_SOCKETS/assets/145742755/db05b1ff-68fe-4fd7-8463-e1e759193912)

## Server:
![image](https://github.com/kannan-nagaraju/3b_CHAT_USING_TCP_SOCKETS/assets/145742755/09fa6ec2-51ae-4531-b650-99f4f3550544)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
