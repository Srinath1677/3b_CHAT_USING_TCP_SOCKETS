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
## Server:
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
## OUTPUT
## Client:
![439248759-d7279a9f-d061-490c-98a7-72fdc58d7512](https://github.com/user-attachments/assets/729b6aed-829c-49d5-ba10-0b532d7bae3f)

## Server:
![439248828-ee91c596-bf2f-469b-b5d0-d83695967baf](https://github.com/user-attachments/assets/7b43ec35-76e0-4271-a06d-4357ef60ccea)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
