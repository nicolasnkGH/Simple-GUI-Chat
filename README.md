# 💬 Simple GUI Chat Application

A lightweight, multi-threaded client-server chat application built using Python. This project demonstrates foundational knowledge of network programming (`socket`), concurrent processing (`threading`), and basic desktop GUI development (`tkinter`).

---

## ✨ Features

* **Client-Server Architecture:** Uses Python's built-in `socket` module for reliable TCP/IP connection establishment and communication.
* **Multi-threading:** The server handles multiple concurrent client connections, and the client application uses separate threads for handling the GUI and receiving incoming messages, ensuring a responsive user experience.
* **Graphical User Interface (GUI):** A simple, functional chat interface built with `tkinter` and a `ScrolledText` widget for managing long chat histories.
* **User Nicknames:** Prompts users for a nickname upon connection.
* **Local or Remote Hosting:** Configured for local loopback (`127.0.0.1`) but easily adjustable for hosting on a public IP address (requires port forwarding).

---

## 🛠️ Technology Stack

| Component | Library/Module | Purpose |
| :--- | :--- | :--- |
| **Backend/Network** | `socket` | Handles connection binding, listening, and TCP data transfer. |
| **Concurrency** | `threading` | Allows the server to manage multiple clients simultaneously and the client GUI to remain responsive. |
| **Frontend/GUI** | `tkinter` | Used for creating the cross-platform graphical interface (windows, buttons, text areas). |
| **I/O Management** | `tkinter.scrolledtext` | Efficiently displays and manages the chat history. |
| **Language** | Python 3 | The core programming language used for all modules. |

---

## 🚀 Installation & Usage

This application requires Python 3 and no external package dependencies (all libraries are standard Python modules).

### Prerequisites

* Python 3.x installed on your system.

### 1. Start the Server

1.  Open a terminal or command prompt.
2.  Navigate to the directory containing `server.py`.
3.  Run the server file:
    ```bash
    python server.py
    ```
    *You should see the output: `Server running...`*

### 2. Run the Client(s)

1.  Open a **separate** terminal or command prompt window for each client you want to launch.
2.  Navigate to the directory containing `client.py`.
3.  Run the client file:
    ```bash
    python client.py
    ```
4.  A popup window will appear, prompting you to **choose a nickname**. Enter your nickname and click OK.
5.  The chat GUI will open, and you can begin sending messages.

**Note:** The client and server are configured to use `HOST = '127.0.0.1'` and `PORT = 9090` by default. If running across a network, ensure these values match and any necessary firewall rules/port forwarding are configured.

---

## 💡 How to Scale (Portability)

To host this application over a local network (LAN) or the public internet:

1.  **Server Side (`server.py`):** Change `HOST = '127.0.0.1'` to your **public IP address** or **internal LAN IP address**. For external hosting, you must also configure port forwarding for `PORT = 9090` on your router.
2.  **Client Side (`client.py`):** Clients must update `HOST = '127.0.0.1'` to match the server's public or internal IP address.
