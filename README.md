# MultiThreaded-Server

Create me a readme.md file
# Java Multi-threaded Client Example

This project demonstrates a simple multi-threaded Java client that connects to a server using sockets. The client spawns 100 threads, each of which connects to a server running on `localhost` at port `8010`, sends a greeting message, and prints the server's response.

## Features

- Uses Java sockets for network communication.
- Demonstrates multi-threading by launching 100 concurrent client connections.
- Each client thread sends a message and prints the server's response.

## How It Works

- The `Client` class contains a `getRunnable()` method that returns a `Runnable` object.
- Each thread created runs this `Runnable`, which:
  - Connects to the server at `localhost:8010`.
  - Sends a message: `"Hello from Client <local address>"`.
  - Waits for and prints the server's response.
- The main method starts 100 such threads.

## Usage

1. **Compile the code:**
   ```
   javac Client.java
   ```

2. **Ensure you have a server running on `localhost` at port `8010`** that can accept connections and respond to messages.

3. **Run the client:**
   ```
   java Client
   ```

## Notes

- This client expects a server to be running and listening on port 8010.
- The server should be able to handle multiple simultaneous connections.
- The code uses try-with-resources to ensure sockets and streams are closed properly.

## Example Output
