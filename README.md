# 3b.CREATION FOR CHAT USING TCP SOCKETS
# Name: LOKESH REDDY A
# Reg No: 212223040104
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.

## PROGRAM
### CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT
### CLIENT:
![image](https://github.com/Lokeshreddya31/3b_CHAT_USING_TCP_SOCKETS/assets/144870682/b01c9a67-1691-4e1f-93b5-b3efef07b212)

### SERVER:
![image](https://github.com/Lokeshreddya31/3b_CHAT_USING_TCP_SOCKETS/assets/144870682/841b9923-8579-4e33-bca0-3a31bfce3029)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
