# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## NAME:KEERTHIKA M P
## REG NO: 212223240071
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client
```
import socket 
s=socket.socket() 
s.connect(('localhost',90)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## server
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
```
## OUPUT
![Screenshot 2024-10-26 221140](https://github.com/user-attachments/assets/631ad63b-73a8-4b87-8fb9-326b6197de53)
![Screenshot 2024-10-26 221150](https://github.com/user-attachments/assets/c7ff8ad8-65a3-4254-95dd-93ac7a61935f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
