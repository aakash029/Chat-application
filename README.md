# Chat-application
Project Structure

.
├── server

│   └── ChatServer.java

└── client

    └── ChatClient.java

    
server/ChatServer.java: This is the main server program. It listens for incoming client connections, manages connected clients, and broadcasts messages.

client/ChatClient.java: This is the client application that connects to the server, sends user input, and receives messages from other users.

 #Features
 

 #Multi-client Support

The server can handle multiple clients concurrently using threads and a thread-safe set.

# Username Identification

Upon connecting, each client must provide a username.

Messages are prefixed with the sender's username, and join/leave notifications are broadcasted.

# Message Broadcasting

Messages from one client are broadcast to all other clients, except the sender.

# Clean Disconnection

If a client disconnects or exits, the server:

Removes the client from the active list.

Broadcasts a "left the chat" message.

# Simple Text-based Protocol

All interactions are done via standard input/output.

Easy to extend (e.g., commands like /list, /whisper).

#How to Run

# Prerequisites

Java 8 or later

Terminal or command prompt

 Compilation
 
In the root directory:

javac server/ChatServer.java client/ChatClient.java

#Start the Server

java server.ChatServer

you should see

Starting chat server on port 12345

Start client in several terminal

java client.ChatClient

Each client will be prompted:

Enter your username:


Then you can start chatting!

Future Enhancements

Add private messaging (/w username message)

Add command handling (/list, /quit)

Add message timestamps

GUI client using Swing or JavaFX

License

This project is open-source and free to use for learning or enhancement purposes.
