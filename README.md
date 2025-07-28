 🔗 Arduino Inter-Device Communication System

This project demonstrates reliable communication between two Arduino boards (Master & Slave) using the Serial protocol. It features a custom packet structure, simulated sensor responses, and robust retry mechanisms.

<br>

## 🚀 Features

- 📤 Master sends commands like `PING`, `STATUS`, and `GET_UPTIME`
- 📥 Slave responds with real-time or simulated data
- ⏳ Timeout and retry logic implemented on Master
- 📋 Logging support and fault simulation
- 🧪 Command parsing with state handling

<br>

## 🛠️ Technologies Used

- Arduino Uno
- Serial Communication (UART)
- Arduino IDE 2.3.6
- C/C++ Embedded Programming

<br>

## 🧩 Communication Protocol

### Packet Format:

| Field        | Value   | Description              |
|--------------|---------|--------------------------|
| START_BYTE   | `0x02`  | Start of packet          |
| COMMAND      | `0x01+` | Command identifier       |
| DATA         | `0x00`  | Dummy or real data       |
| END_BYTE     | `0x03`  | End of packet            |

### Example:
Master sends: [0x02, 0x01, 0x00, 0x03] // CMD_PING
Slave replies: [0x02, 0xAA, 0x03] // PONG

<br>

## 📂 Project Structure

arduino-interdevice-communication/
├── master/
│ └── master.ino
├── slave/
│ └── slave.ino
├── docs/
│ └── protocol.md
├── images/
│ └── screenshot-*.png
└── README.md

<br>

## 🖼️ Screenshots

### 1️⃣ Master Serial Output with Retry Logic  
![Master Timeout and Retry]((https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20112006.png))

### 2️⃣ Successful UPTIME, PING, STATUS Communication  
![Master Success Output](https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20112102.png)

### 3️⃣ Consistent Output of Uptime, PONG, and STATUS  
![Master Response Flow](https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20121017.png)

### 4️⃣ Final Stable Serial Monitor View  
![Master-Slave Final Working](https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20121051.png)

### 5️⃣ Slave Log Handling and Event Storage  
![Slave Logs Display](https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20122048.png)

### 6️⃣ Complete Log and Temperature Simulation Output  
![Logs & Temp Simulation](https://github.com/Prabhudev2004/Arduino-Inter-Device-Communication-System/blob/913727a59552f6d6234d89cf442032180b80b4b6/Screenshot%202025-07-24%20122118.png)

> 📌 Make sure you rename your uploaded screenshots to match the above file names (inside an `images/` folder in the repo).

<br>

## 📌 Weekly Progress

### Week 1 – Setup & Protocol Design
- Serial communication tested between Arduinos
- Basic wiring completed
- Command structure and protocol finalized

### Week 2 – Core Communication
- Master can send multiple commands
- Slave parses and responds correctly
- Retry and timeout logic implemented

### Week 3 – Data Simulation & State Handling
- Slave maintains uptime, temperature, and log responses
- Fault simulation (delay, drop) tested

### Week 4 – Final Testing & Documentation
- Command-response system fully functional
- Screenshots recorded and documentation complete

<br>

## 👨‍💻 Team & Roles

| Team Member       | Contribution                     |
|-------------------|----------------------------------|
| **Amogh & Prabhu**   | Master Controller Development     |
| **Soujanya & Prabhu**| Slave Device Development         |

<br>



---
