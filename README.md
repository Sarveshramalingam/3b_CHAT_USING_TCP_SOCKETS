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
server.py
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
client.py
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

```
## OUPUT
<img width="1266" height="167" alt="image" src="https://github.com/user-attachments/assets/61bf87ce-e334-48b0-93cf-d37dac85d91a" />
<img width="1266" height="167" alt="image" src="https://github.com/user-attachments/assets/7b523f5d-b40e-4a55-9355-958bedd491cd" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
