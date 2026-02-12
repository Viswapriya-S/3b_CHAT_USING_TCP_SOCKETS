# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
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
## OUPUT
SERVER

<img width="1172" height="312" alt="Screenshot 2026-02-12 113415" src="https://github.com/user-attachments/assets/4884f409-1c4f-41dc-b0e1-4d42c30b45ea" />

CLIENT

<img width="1057" height="308" alt="Screenshot 2026-02-12 113433" src="https://github.com/user-attachments/assets/22173b7c-40a5-4cde-87c8-3b33bbc83266" />

## RESULT
Thus, the python program for creating chat using TCP Sockets Links was successfully
created and executed.

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
