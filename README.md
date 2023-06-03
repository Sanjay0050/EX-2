# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

## DATE: 15.03.2023
 
## AIM :
To write a python program to perform stop and wait protocol
ALGORITHM :

1.Start the program. 
2.Get the frame size from the user
3.To create the frame based on the user request. 
4.To send frames to server from the client side.
5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client. 
6.Stop the program
## PROGRAM :
## CLIENT :
```
#Developed by :  SANJAY.P
#Register Number : 212221220047
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
 ```
## SERVER :
```
#Developed by : SANJAY.P
#Register Number : 212221220047
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received".encode())
```
## OUTPUT :
## CLIENT:
![242247658-5e3db979-dc45-41d4-b6f6-1bc44005acaf](https://github.com/Amruthavarshnibs/EX-2/assets/119103704/f1834824-b896-4f5b-8a43-6560a89d6674)
## SERVER:
![242247785-4470e7c7-1ce6-4fe3-a925-523f5ad6db6c](https://github.com/Amruthavarshnibs/EX-2/assets/119103704/bee5064b-51f3-45db-8a02-8e1235c50029)



## RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.

