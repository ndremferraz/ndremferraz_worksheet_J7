# Worksheet: J7

## Question 1: What is inside a packet 
Inside a packet there is the Header that contains the destination address for the data and the payload that is the data itself or the message that is being sent. 

## Question 2: What is the purpose of an internet layer in the TCP/IP protocol? What do you, as a client, need to specify in this protocol?
The internet layer of the TCP/IP protocol is to use of the multiple computer networks from get information from point A to point B. As the client you need to specify the IP address. 

## Question 3: What is the purpose of the transport layer in the TCP/IP protocol? What do you, as a client, need to specify in the protocol?
The transport layer of the TCP/IP protocol is meant to simplify the use of the internet and the multiple networks. As a client you need to specify the destination port.  

## Question 4: What is the difference between SMTP and HTTP?
SMTP is used to transport email messages and HTTP is used to download web content. 

## Question 5: What is the difference between and IP address and a domain name?
The IP address is the internet protocol address for a network device, is something used by the internet protocol to comunicate data to an appropriate device. The domain name the is human accessible form of identifying a devices address. However, one domain can have multiple IP addresses.

## Question 6: How does the operating System use ports?
The Operating System uses ports to organize and process the data arriving from the network based on the process being acomplished.

## Question 7: Write code that creates a socket connection to ip address 123.45.678.900 at port 4040. Then, print a color to that socket's output.
```java
public static void main(String[] args){
  Socket sock = null;
  try{
    sock = new Socket("123.45.678.900", 4040);
  }catch {
    System.err.println("Cannot conect");
    System.exit(1);
  }

  try{
    PrintWriter pw = new PrintWriter(sock.getOutputStream());
    pw.println("Blue");
    pw.close();
    sock.close();
  } catch(Exception e){
    System.err.print("IOException");
    System.exit(1);
  }
}


```

## Question 8: What is the difference betweeen a socket's inputs stream and its output stream?
The socket's input stream recieves a stream from the server, and the output stream sends a stream to the server. 

## Question 9: What is the difference between a Socket and a SocketServer?
SocketServer is a class made to implement servers that will pass on the data to the Clients, the Socket Objects. 

## Question 10: How are threads useful with servers? How does a server manage to always be listening for sockets trying to connect?
Threads are useful with servers because multiple threads can be created to process multiple requests. A server always keep an open socket awaiting for incoming comunication. 
