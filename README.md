# 🛰️ WebSocket Chat Server

A simple WebSocket server built with Node.js using the [`ws`](https://github.com/websockets/ws) library.  
It supports real-time communication with both **broadcast** and **private messaging** features using **username-based identification**.

---

## 🚀 Features

- 🌐 Real-time WebSocket communication
- 👤 Username assignment for each client
- 📣 Broadcast messaging (to all clients except the sender)
- 🔒 Private messaging (to a specific client)
- 🧼 Clean and modular code for easy customization

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/websocket-chat-server.git
   cd websocket-chat-server
Install dependencies:

bash
Copy
Edit
npm install
🛠️ Usage
Start the server
js
Copy
Edit
// index.js
const Start = require('./Start'); // Adjust path if needed

const PORT = 8080;
const server = new Start(PORT);
server.startServer();
Then run:

bash
Copy
Edit
node index.js
You’ll see:

nginx
Copy
Edit
Broadcast server started on ws://localhost:8080
🔌 WebSocket Client Example
js
Copy
Edit
const socket = new WebSocket('ws://localhost:8080');

// Set your username
socket.send(JSON.stringify({ set_username: "Alice" }));

// Send a broadcast message
socket.send(JSON.stringify({ broadcast_msg: "Hello, everyone!" }));

// Send a private message to another user
socket.send(JSON.stringify({ private_msg: "Hi Bob!", to: "Bob" }));
📤 Message Format (Client → Server)
Action	JSON Format Example
Set username	{ "set_username": "Alice" }
Broadcast message	{ "broadcast_msg": "Hello!" }
Private message	{ "private_msg": "Hey!", "to": "Bob" }

📥 Server Responses (Server → Client)
Broadcast messages:

yaml
Copy
Edit
Broadcast message: Alice: Hello!
Private messages:

vbnet
Copy
Edit
Private Message Alice: Hey!
📁 File Structure
pgsql
Copy
Edit
.
├── Start.js          # WebSocket server class
├── index.js          # Entry point to start the server
├── package.json
└── README.md
✅ TODOs / Ideas for Improvement
 Add user disconnect handling

 Prevent duplicate usernames

 Add typing indicators

 Add message history per client

 Create simple frontend chat client

📄 License
This project is licensed under the MIT License.

👨‍💻 Author
Kaverappa ck
Feel free to reach out or contribute via PRs!
