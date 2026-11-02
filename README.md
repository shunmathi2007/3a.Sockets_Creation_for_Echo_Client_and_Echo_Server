# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
import socket 

s=socket.socket() 

s.connect(('localhost',8000)) 

while True:

    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
## SERVER
import socket 

s=socket.socket() 

s.bind(('localhost',8000))

s.listen(5) 

c,addr=s.accept() 

while True: 

    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
## OUPUT
<img width="1037" height="240" alt="WhatsApp Image 2026-11-02 at 2 19 17 PM" src="https://github.com/user-attachments/assets/7709b81f-8ca1-4c2c-8130-e875caa0d3b9" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
