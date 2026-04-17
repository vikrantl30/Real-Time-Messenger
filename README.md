# Real-Time-Messenger
A simple real-time chat application built using **Spring Boot, WebSockets, STOMP, and SockJS** that allows multiple users to communicate instantly without refreshing the page.

---

## 🧠 Overview

This project demonstrates how real-time communication works using persistent connections instead of traditional request-response APIs.

Users can:

* Join the chat
* Send messages
* Receive messages instantly from all connected users

---

## ⚙️ Tech Stack

* **Backend:** Spring Boot
* **Real-time Communication:** WebSockets
* **Protocol:** STOMP
* **Fallback:** SockJS
* **Frontend:** HTML, CSS, JavaScript

---

## 🔁 How It Works

```
1. Client connects to server via /chat
2. Connection stays open (WebSocket)
3. Client subscribes to /topic/messages
4. User sends message → /app/sendMessage
5. Server receives message
6. Message broker broadcasts → /topic/messages
7. All connected clients receive message instantly
```

---

## 🧩 Key Concepts Implemented

### 🔹 WebSockets

* Enables **persistent, two-way communication**
* Eliminates need for repeated HTTP requests

### 🔹 STOMP (Simple Text Oriented Messaging Protocol)

* Defines how messages are structured
* Uses destinations like:

  * `/app` → client to server
  * `/topic` → server to clients

### 🔹 SockJS

* Provides fallback options if WebSockets are not supported
* Ensures reliable connection across browsers

### 🔹 Message Broker

* Handles **message distribution**
* Broadcasts messages to all subscribed clients efficiently

---

## 🧪 Features

* Real-time messaging
* Multiple users support
* No page refresh required
* Lightweight frontend UI

---

## 🧱 Project Structure

```
com.chat.app
│
├── config
│   └── WebSocketsConfig.java
│
├── controller
│   └── ChatController.java
│
├── model
│   └── ChatMessage.java
│
└── templates
    └── chat.html
```

---

## ⚠️ Challenges Faced

* Understanding WebSocket lifecycle and connection handling
* Differentiating between `/app` and `/topic` message flow
* Debugging connection issues during initial setup
* Synchronizing frontend and backend communication

---

## 🚀 Future Improvements

* Private messaging (1-to-1 chat)
* Store messages in database (MongoDB/MySQL)
* User authentication (JWT)
* Online/offline user status
* Typing indicators

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Run Spring Boot application

3. Open browser:

```bash
http://localhost:8080/chat
```

---

## 📌 Learning Outcome

This project helped in understanding:

* Real-time system design basics
* Event-driven communication
* How scalable messaging systems work

---

## 📷 Demo (Add this)

👉 Add a GIF or screenshot here for better visibility

---

## 🔗 Connect

If you're working on similar projects or have suggestions, feel free to connect.

---

