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
## CLIENT
```py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```py
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
## CLIENT
![Screenshot 2024-04-12 142538](https://github.com/codedbykishore/3b_CHAT_USING_TCP_SOCKETS/assets/147139122/89777ca3-dbef-498e-9721-6d3174e50e15)
## SERVER
![Screenshot 2024-04-12 142549](https://github.com/codedbykishore/3b_CHAT_USING_TCP_SOCKETS/assets/147139122/7ab00228-1467-4195-8c49-02e984b69aeb)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
