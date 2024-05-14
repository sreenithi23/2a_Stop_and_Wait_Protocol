# 2a_Stop_and_Wait_Protocol
NAME:SREENITHI.E
REG NO:212223220109
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
```
```
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program

``
## PROGRAM
```
````
## Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
``````
``````
## server

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
```
## OUTPUT
client
![image](https://github.com/sreenithi23/2a_Stop_and_Wait_Protocol/assets/147017600/0243899d-33b5-4e15-843e-200121bd4189)
server
![image](https://github.com/sreenithi23/2a_Stop_and_Wait_Protocol/assets/147017600/54eee5bb-9960-4e62-9de3-9e70258f9d12)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
