


Welcome to your networking and client-server architecture task. This project aims to give you hands-on experience with essential concepts in networking and how client-server applications work. The task is designed to be approachable for both students with and without prior coding experience.

#### Purpose of the Task:

1. **Understanding Networking Basics**:
    
    - You'll learn the fundamental concepts of networking, such as IP addresses, subnetting, and the differences between TCP and UDP. These concepts are crucial for understanding how devices communicate over a network.
    - **Tools Used**: Basic network diagnostic tools like ping and traceroute
    
1. **Client-Server Architecture**:
    
    - You'll explore the client-server model, a fundamental concept where clients request services and servers provide them. Understanding this architecture is critical for developing and troubleshooting networked applications.
    - **Tools Used**: Simple theoretical explanations and practical demonstrations.
3. **Practical Implementation**:
    
    - **With Coding Experience**: You will develop a basic client-server application using Python. This will involve writing scripts for both the server and the client, allowing you to see first-hand how data is exchanged in a network.
    - **Without Coding Experience**: You will focus on understanding and documenting the process. You’ll be guided step-by-step through running pre-written scripts, and you'll learn how these scripts function without needing to write code yourself.
4. **Network Simulation with Cisco Packet Tracer**:
    
    - **For All Students**: You'll use Cisco Packet Tracer to create a visual and interactive simulation of a network. This tool will help you understand the flow of packets between a client and a server and how different network devices interact.
    - **Tools Used**: Cisco Packet Tracer to design, configure, and analyse a network.
5. **Comprehensive Learning**:
    
    - **For All Students**: By the end of this task, you’ll have a deeper understanding of both the theoretical and practical aspects of networking and client-server architecture. You'll be able to configure a simple network, understand the flow of data, and analyse network traffic.

#### Task Outline:

1. **Networking Basics**:
    
    - Write a report on key networking concepts.
    - Perform and document network diagnostics (ping, traceroute).
2. **Client-Server Architecture**:
    
    - Write a report on the client-server model.
    - Run and understand Python scripts for a simple client-server application.
3. **Network Simulation with Packet Tracer**:
    
    - Create and configure a network in Packet Tracer.
    - Simulate and analyse packet flow between client and server.
4. **Documentation**:
    
    - Document all your findings, configurations, and analyses.

#### Submission:

Submit the following:

- Reports on networking basics and client-server architecture.
- Source code and documentation for the client-server application (if applicable).
- Packet Tracer file and analysis documentation.

### Additional Instructions:

- **If you have Coding Experience**: Focus on understanding the scripts and try to modify or extend them for additional learning.
- **If you don't have Coding Experience**: Focus on understanding the concepts and the flow of the scripts. Use the provided documentation to run and test the scripts.

***Feel free to ask questions or seek help if you encounter any difficulties. This task is designed to be a learning experience, and support is available if needed.***


---


> [!NOTE] NOTE
> ***Feel free to ask questions or seek help if you encounter any difficulties. This task is designed to be a learning experience, and support is available if needed.***



# TASK

#### Objective:

To understand and implement the concepts of networking and client-server architecture by developing a basic application that demonstrates communication between a client and a server.

#### Requirements:

1. **Programming Languages**: Python (or any other preferred language)
2. **Tools**: Any text editor or IDE, network simulator (like Packet Tracer) if needed, and basic networking tools (ping, netstat, etc.)
3. **Knowledge**: Basic understanding of networking concepts, socket programming, and client-server architecture

#### Task Details:

1. **Setup the Environment**:
    
    - Install necessary software (Python, IDE, etc.).
    - Ensure network tools are available (ping, traceroute, etc.).
2. **Networking Basics**:
    
    - Write a brief report explaining the following concepts:
        - IP addresses (IPv4 vs. IPv6)
        - Subnetting
        - TCP vs. UDP
        - DNS
    - Perform and document the following network diagnostics on your machine:
        - Ping a website (e.g., google.com) and document the results.
        - Use `traceroute` (or `tracert` on Windows) to trace the route to a website.
3. **Client-Server Architecture**:
    
    - Write a brief report explaining the client-server model.
    - Differentiate between synchronous and asynchronous communication.
    - Explain the roles of the client and the server in a network.
4. **Develop a Client-Server Application**:
    
    - **Server**:
        - Write a Python script to create a simple server that listens on a specific port.
        - The server should accept connections from clients and respond to a simple request (e.g., sending back a "Hello, Client!" message).
    - **Client**:
        - Write a Python script to create a client that connects to the server.
        - The client should send a request to the server and display the response.



### example

```python
# Server Script (server.py)
import socket

def start_server():
    server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    server_socket.bind(('localhost', 12345))
    server_socket.listen(5)
    print("Server is listening on port 12345...")

    while True:
        client_socket, addr = server_socket.accept()
        print(f"Connection from {addr} has been established.")
        client_socket.send(bytes("Hello, Client!", "utf-8"))
        client_socket.close()

if __name__ == "__main__":
    start_server()

```


``` python
# Client Script (client.py)
import socket

def connect_to_server():
    client_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    client_socket.connect(('localhost', 12345))
    message = client_socket.recv(1024)
    print(message.decode("utf-8"))
    client_socket.close()

if __name__ == "__main__":
    connect_to_server()

```



1. **Testing and Documentation**:
    
    - Run the server script and ensure it is listening for connections.
    - Run the client script to connect to the server and verify that it receives the correct response.
    - Document the steps taken to run and test the application.
    - Include screenshots or logs showing the server and client interaction.
2. **Submission**:
    
    - Submit the following:
        - Source code for both client and server scripts.
        - Report on networking basics and client-server architecture.
        - Documentation of the testing process and results.


#Note

```
in this task you should implement error handling in the scripts.
add additional features like multi-threading for handle multiple client connections.
```





