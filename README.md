# Java Console Chat Application

## Overview
This project is a simple console-based chat application built using Java sockets. It follows a client-server architecture where multiple clients can connect to a server and exchange messages in real time through the terminal.

The project demonstrates the basics of network programming in Java, including socket communication, input/output streams, and multithreading.

## Architecture

The system follows a **client-server model**:

- **Server**: Listens for incoming connections and manages communication between connected clients.
- **Client**: Connects to the server and allows the user to send and receive messages.
- **ClientHandler**: A thread created by the server to handle each connected client.

## Components

### Server
The server is responsible for:
- Listening for incoming client connections.
- Accepting socket connections.
- Creating a new thread for each client.
- Broadcasting messages to all connected clients.

### Client
The client is responsible for:
- Connecting to the server using a socket.
- Sending messages entered by the user.
- Receiving and displaying messages from other users.

### ClientHandler
The ClientHandler class manages communication between the server and a specific client. It typically runs in its own thread and:
- Reads messages from the client.
- Sends messages to the server.
- Handles client disconnection.

## Technologies Used

- **Java**
- **Java Networking (Sockets)**
- **BufferedReader**
- **BufferedWriter**
- **Multithreading**

## How the Communication Works

1. The server starts and listens on a specified port.
2. A client connects to the server using the server’s IP address and port.
3. The server accepts the connection and creates a `ClientHandler` thread.
4. The client sends messages to the server.
5. The server receives the message and broadcasts it to all connected clients.

## Running the Project

### 1. Compile the project

```bash
javac Server.java Client.java ClientHandler.java
