# 3b.CREATION FOR CHAT USING TCP SOCKETS
### Name: Ezhil Nevedha K
### Reg.no: 212223230055
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py:
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
![image](https://github.com/user-attachments/assets/e540f832-9029-460f-9290-6284fbcd93b0)
![image](https://github.com/user-attachments/assets/ddf27822-8592-46cc-901a-1f50a70769bf)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
