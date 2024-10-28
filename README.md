# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME : SHYAM R
### REG NO : 21223040200
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("Server>",s.recv(1024).decode())
    

```
### Server:
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c.addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client>",ClientMessage)
    msg=input("Server>")
    c.send(msg.encode())

```
## OUPUT
### Client:
![image](https://github.com/user-attachments/assets/62e331e1-9319-40b6-bf5a-bbb7953b2e77)

### Server:
![image](https://github.com/user-attachments/assets/924d82fe-7a89-4874-b43a-3f84823284c5)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
