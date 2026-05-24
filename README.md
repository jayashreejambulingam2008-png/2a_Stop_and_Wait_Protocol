# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
Name: JAYASHREE J
Register Number: 212225040145

CLIENT:
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
    else:
        c.close()
        break

SERVER:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```

## OUTPUT

CLIENT:

<img width="1600" height="898" alt="image" src="https://github.com/user-attachments/assets/76a501a7-e0a4-4965-9164-dd518b746dd3" />

SERVER:

<img width="1600" height="895" alt="image" src="https://github.com/user-attachments/assets/56095e9a-d1ad-47c3-ab2a-1eb1fed8b96a" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
