# Real-Time Anonymous Chat Architecture

**Bachelor of Engineering (Computer Science) Final Year Project**

🟢 **[View the Live Application Here](https://chatapplication-c4q2n4la.b4a.run/)**

> **Note to Reviewers (2026 Update):** The core backend architecture, socket connections, and routing logic of this project remain exactly as they were submitted for my final year degree evaluation in 2023. Recently, the `README.md` and basic CSS styling were updated to improve documentation and accessibility for portfolio review purposes, alongside 1-2 minor bug patches to ensure the application runs smoothly in current environments. The underlying engineering reflects my original undergraduate work.

## Overview

This repository contains the software implementation for my Bachelor of Engineering final year capstone project. The primary objective was to design, build, and deploy a highly responsive, real-time communication system capable of pairing users dynamically while maintaining low-latency message delivery and secure connections.

## Technical Architecture & Stack

The application utilizes an event-driven architecture to handle concurrent WebSocket connections efficiently, ensuring real-time bidirectional data flow between the client and server.

- **Backend Environment:** Node.js
- **Web Framework:** Express.js
- **Real-Time Communication:** Socket.io
- **Frontend:** JavaScript, HTML5, CSS3

## Core Engineering Features

- **Dynamic Connection Pooling:** The server automatically pairs available users into isolated communication channels. If no users are available in the pool, incoming connections are queued until a peer connects.
- **State Management & Lifecycle Handling:** Efficiently manages connection states, graceful disconnects, and session terminations, ensuring no ghost connections remain active when a user drops off.
- **Event-Driven Notifications:** Implements browser-level API integrations to alert users of incoming payloads when the application state or browser tab is unfocused.
- **Input Sanitization & Parsing:** Detects and formats specific string patterns in real-time. This includes URL parsing to render safe clickable links and system action commands (e.g., parsing `/me [action]` into structured system notifications).

## Installation and Local Deployment

To run this project locally on your machine, ensure you have Node.js installed, then follow these steps:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Naveen7271/Chat-application.git](https://github.com/Naveen7271/Chat-application.git)
   cd Chat-application
   ```

## Installation and Local Deployment

To run this project locally on your machine, ensure you have Node.js installed, then follow these steps:

1. **Clone the repository:**

   ```bash
   git clone [https://github.com/Naveen7271/Chat-application.git](https://github.com/Naveen7271/Chat-application.git)
   cd Chat-application
   Install the necessary backend dependencies:
   npm install express socket.io
   ```

2. **Initialize the Node server:**

   ```bash
   node app.js
   ```

3. **Access the client:**
   ```
   Open a web browser and navigate to http://localhost:5050 (or the port specified in your console output). To test the pairing logic, open the link in two separate browser windows or tabs.
   ```

## License

This project is licensed under the GNU General Public License v3.0.
