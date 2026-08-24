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
# CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

# SERVER
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
# CLIENT
<img width="807" height="1012" alt="Screenshot 2026-08-21 215809" src="https://github.com/user-attachments/assets/a57e2815-3ade-4f5f-8cb7-49d53006742d" />

# SERVER
<img width="989" height="1000" alt="Screenshot 2026-08-21 215817" src="https://github.com/user-attachments/assets/1ff4bf44-75c3-4839-a869-e19cb6e78145" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
