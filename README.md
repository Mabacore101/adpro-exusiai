# Experiment README
## Experiment 2.1: Original code, and how it run
![alt text](/img/BroadcastSS1.png)  
![alt text](/img/BroadcastSS2.png)  
![alt text](/img/BroadcastSS3.png)  
![alt text](/img/BroadcastSS4.png)  
- From the output above, we can see that the server acts as a listener and receives connections from each client. The server receives and distributes new messages as they are sent. Each client can create messages and receive messages from other connected clients, with the server handling the processing.

## Experiment 2.2: Modifying port
![alt text](/img/BroadcastSS5.png)  
![alt text](/img/BroadcastSS6.png)  
![alt text](/img/BroadcastSS7.png)  
![alt text](/img/BroadcastSS8.png)  
- If we change both the server and client ports with the same port number, the app works fine just like the picture above.
![alt text](/img/BroadcastSS9.png)  
- However, if we change only 1 port (either client or server), we will get an error. This is because the client can't find the target server with the corresponding port just like the picture above.

## Experiment 2.3: Small changes, add IP and Port
![alt text](/img/BroadcastSS10.png) 
![alt text](/img/BroadcastSS11.png) 
![alt text](/img/BroadcastSS12.png) 

- I added the information from `Mabacore101's computer` to both the server and client. I added `bcast_tx.send(format!("{addr} : {text}"))?;` to send a broadcast message with the format of the address and the text so that all clients receive information from each other's addresses. Then, I also added `println!("New connection from Mabacore101's computer {addr:?}");` to display a message indicating that a connection to the server from `Mabacore101's computer` has occurred.