# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME:SANJAY ASHWIN P
## REG NO:212223040181
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
### client:
import socket    
s=socket.socket()   
s.bind(('localhost',8000))   
s.listen(5)   
c,addr=s.accept()   
while True:   
    clientMessage=c.recv(1024).decode()  
    c.send((clientMessage.encode()))   
### server:
import socket      
s=socket.socket()   
s.connect(('localhost',8000))   
while True:   
    msg=input("client>")  
    s.send(msg.encode())  
    print("server>",s.recv(1024).decode())   
## OUPUT
### client:
![Screenshot 2024-04-09 174413](https://github.com/sanjayashwinP/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147473265/ceebbedf-678b-412d-8c11-8aaedfcae3c2)
### server:
![Screenshot 2024-04-09 174718](https://github.com/sanjayashwinP/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147473265/9dacb1b7-4752-4d76-97d0-918a350fac20)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
