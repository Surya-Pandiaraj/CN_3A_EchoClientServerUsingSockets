### NAME: SURYA P <br>
### REG NO: 212224230280

## EX. No. 3a : ECHO CLIENT AND SERVER USING SOCKETS 

# AIM :

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server .
4. Send and receive the message using the send function in socket.

## PROGRAM :

## client.py :

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## server.py :

```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```

## OUPUT :

### client.py

<img width="639" height="200" alt="image" src="https://github.com/user-attachments/assets/c0978722-dbd6-418c-a53b-dd997b3839f7" />

### server.py

<img width="676" height="57" alt="image" src="https://github.com/user-attachments/assets/6fe25915-39ea-46cc-b4be-a8917b8fdb87" />

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
