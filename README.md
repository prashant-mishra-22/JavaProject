# Disaster Resource Management System (DRMS)

<div align="center">

![Java](https://img.shields.io/badge/Java-8%2B-red)
![Client-Server](https://img.shields.io/badge/Architecture-Client--Server-blue)
![MySQL](https://img.shields.io/badge/Database-MySQL-orange)
![Multi-threading](https://img.shields.io/badge/Concurrency-Multi--threading-green)
![Socket](https://img.shields.io/badge/Network-Java%20Sockets-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Contributors](https://img.shields.io/badge/Contributors-6-yellow)
![NIT Patna](https://img.shields.io/badge/NIT-Patna-important)

**A Java-based Client-Server System for Real-time Disaster Resource Coordination and Management**

</div>

## 👥 Team Members
<div align="center">

| Member | Roll No | GitHub | Role |
|--------|---------|--------|------|
| **Rishi Kumar** | 2447031 | [@rishikr507](https://github.com/rishikr507) | Headquarter Module Lead |
| **Prashant Kumar Mishra** | 2447021 | [@prashant-mishra-22](https://github.com/prashant-mishra-22) | Server Architecture Lead |
| **Satyam Bhardwaj** | 2447052 | [@ijugunu](https://github.com/ijugunu) | Camp Module Development |
| **Mayank Shaw** | 2447050 | [@mayankshaw20](https://www.linkedin.com/in/mayankshaw20/) | Camp Module Development |
| **Monil Mishra** | 2447017 | [@mishramonil](https://www.instagram.com/mishramonil/) | Database & Integration |
| **Biswajit Ghadei** | 2447036 | [@biswajit-ghadei](https://www.linkedin.com/in/biswajit-ghadei-aa6588201/)| Database & Utilities |

</div>

## 🏆 Badges

<div align="center">

[![Java Version](https://img.shields.io/badge/Java-8%2B-red)](https://www.java.com/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0%2B-blue)](https://www.mysql.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/prashant-mishra-22/JavaProject?style=social)](https://github.com/prashant-mishra-22/JavaProject/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/prashant-mishra-22/JavaProject?style=social)](https://github.com/prashant-mishra-22/JavaProject/network/members)
[![GitHub issues](https://img.shields.io/github/issues/prashant-mishra-22/JavaProject)](https://github.com/prashant-mishra-22/JavaProject/issues)
[![GitHub pull requests](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/prashant-mishra-22/JavaProject/pulls)
[![Last Commit](https://img.shields.io/github/last-commit/prashant-mishra-22/JavaProject)](https://github.com/prashant-mishra-22/JavaProject/commits/main)

</div>

## 🛠️ Technical Stack

<div align="center">

| **Component** | **Technology** | **Purpose** |
|--------------|----------------|-------------|
| **Core Language** | ![Java](https://img.shields.io/badge/Java-ED8B00?logo=java&logoColor=white) | Application Development |
| **Database** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white) | Data Persistence |
| **Networking** | ![Java Sockets](https://img.shields.io/badge/Java%20Sockets-007396?logo=java&logoColor=white) | Client-Server Communication |
| **Concurrency** | ![Multi-threading](https://img.shields.io/badge/Multi--threading-007396?logo=java&logoColor=white) | Concurrent Client Handling |
| **JDBC Driver** | ![JDBC](https://img.shields.io/badge/JDBC-007396?logo=java&logoColor=white) | Database Connectivity |
| **Version Control** | ![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white) | Code Management |

</div>

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [🎯 Objectives](#-objectives)
- [🏗️ System Architecture](#️-system-architecture)
- [👥 System Actors](#-system-actors)
- [📊 Database Design](#-database-design)
- [⚙️ Installation & Setup](#️-installation--setup)
- [💻 How to Run](#-how-to-run)
- [🔧 Implementation Details](#-implementation-details)
- [🔄 Workflow](#-workflow)
- [📁 Project Structure](#-project-structure)
- [🚧 Challenges Faced](#-challenges-faced)
- [🔮 Future Enhancements](#-future-enhancements)
- [📚 References](#-references)

## 📌 Project Overview

The **Disaster Resource Management System (DRMS)** is a Java-based client-server application designed to streamline disaster relief operations. It provides a centralized platform for real-time coordination between Field Offices (Relief Camps) and Headquarters, enabling efficient resource allocation during emergency situations.

**Key Innovation**: Real-time communication between multiple camps and headquarters with automated request generation, approval workflows, and comprehensive logging for audit trails.

## 🎯 Objectives

1. **Centralized Coordination**: Enable real-time communication between field camps and headquarters
2. **Automated Resource Management**: Automatic request generation when inventory falls below threshold
3. **Concurrent Client Handling**: Support multiple simultaneous client connections
4. **Secure Data Management**: Thread-safe operations and data consistency
5. **Comprehensive Logging**: Maintain audit trails for all system actions
6. **Practical OOP Demonstration**: Apply core Java OOP principles in real-world scenario

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    DRMS SYSTEM ARCHITECTURE                 │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────┐   │
│  │                    CENTRAL SERVER                   │   │
│  │    Multi-threaded • Port 12345 • MySQL Integration  │   │
│  └─────────────────────────────────────────────────────┘   │
│         │                         │                        │
│  ┌──────▼──────┐         ┌───────▼────────┐               │
│  │   CAMPS     │         │  HEADQUARTERS  │               │
│  │ (Multiple)  │         │    (Single)    │               │
│  │ • Register  │         │ • View Requests│               │
│  │ • Request   │◄───────►│ • Approve/Reject              │
│  │ • View Logs │         │ • Monitor All  │               │
│  └─────────────┘         └────────────────┘               │
│         │                         │                        │
│  ┌──────▼─────────────────────────▼──────┐                │
│  │          MySQL DATABASE                │                │
│  │ • camps • resources • requests • logs  │                │
│  └────────────────────────────────────────┘                │
└─────────────────────────────────────────────────────────────┘
```

## 👥 System Actors

### **1. Field Relief Camps (Client Application)**
- **Who**: Front-line relief units serving affected communities
- **Responsibilities**:
  - Register with unique camp ID
  - Manage local resource inventory
  - Generate automated resource requests
  - Track request status in real-time
  - View system logs

### **2. Headquarters (Client Application)**
- **Who**: Central command center (NDRF/SDRF authorities)
- **Responsibilities**:
  - Monitor all active camps
  - View all pending resource requests
  - Approve or reject requests
  - Maintain audit logs
  - Real-time inventory monitoring

### **3. Database System**
- **Who**: Central data repository
- **Function**:
  - Store camp registrations
  - Maintain resource inventories
  - Track request history
  - Log all system activities

## 📊 Database Design

### **Database Schema: `disaster_management`**

```sql
-- 1. CAMPS TABLE
CREATE TABLE camps (
    camp_id INT AUTO_INCREMENT PRIMARY KEY,
    camp_name VARCHAR(100) NOT NULL,
    camp_number INT UNIQUE,
    is_active BOOLEAN DEFAULT true,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- 2. RESOURCES TABLE
CREATE TABLE resources (
    resource_id INT AUTO_INCREMENT PRIMARY KEY,
    camp_id INT NOT NULL,
    resource_name VARCHAR(100) NOT NULL,
    quantity INT DEFAULT 0,
    unit VARCHAR(50),
    FOREIGN KEY (camp_id) REFERENCES camps(camp_id),
    UNIQUE KEY unique_camp_resource (camp_id, resource_name)
);

-- 3. REQUESTS TABLE
CREATE TABLE requests (
    request_id INT AUTO_INCREMENT PRIMARY KEY,
    camp_id INT,
    resource_name VARCHAR(100) NOT NULL,
    amount INT NOT NULL,
    deadline_days INT,
    status ENUM('PENDING', 'APPROVED', 'REJECTED') DEFAULT 'PENDING',
    requested_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    acknowledged_at TIMESTAMP NULL,
    FOREIGN KEY (camp_id) REFERENCES camps(camp_id)
);

-- 4. LOGS TABLE
CREATE TABLE logs (
    log_id INT AUTO_INCREMENT PRIMARY KEY,
    camp_id INT,
    action_type VARCHAR(100),
    description TEXT,
    log_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (camp_id) REFERENCES camps(camp_id)
);
```

### **ER Diagram**
```
     ┌─────────┐      ┌───────────┐      ┌──────────┐
     │  CAMPS  │◄────┤ RESOURCES  │      │  LOGS    │
     ├─────────┤      ├───────────┤      ├──────────┤
     │ camp_id ├─────►│ camp_id   │      │ camp_id  │
     │ camp_no │      │ resource  │      │ action   │
     │ name    │      │ quantity  │      │ desc     │
     │ active  │      │ unit      │      │ time     │
     └─────────┘      └───────────┘      └──────────┘
          │
          │          ┌──────────┐
          └─────────►│ REQUESTS │
                     ├──────────┤
                     │ camp_id  │
                     │ resource │
                     │ amount   │
                     │ status   │
                     │ deadline │
                     └──────────┘
```

## ⚙️ Installation & Setup

### **Prerequisites**
1. **Java JDK 8 or higher**
2. **MySQL Server 8.0+**
3. **MySQL Connector/J 9.3.0**
4. **Git (for cloning repository)**

### **Step-by-Step Setup**

#### **1. Clone Repository**
```bash
git clone https://github.com/prashant-mishra-22/JavaProject.git
cd JavaProject
```

#### **2. Database Setup**
```sql
-- Run the SQL script to create database and tables
mysql -u root -p < Database.sql
```
Or execute manually:
```sql
CREATE DATABASE disaster_management;
USE disaster_management;
-- Copy and paste all CREATE TABLE statements from Database.sql
```

#### **3. Configure Database Connection**
Edit `Server.java` line 70-73:
```java
dbConnection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/disaster_management?useSSL=false&allowPublicKeyRetrieval=true",
    "root",                    // Change username if needed
    "your_password_here"       // Change to your MySQL password
);
```

#### **4. Download MySQL Connector**
Download `mysql-connector-j-9.3.0.jar` from:
https://dev.mysql.com/downloads/connector/j/

Place it in your project directory.

## 💻 How to Run

### **Compilation**
```bash
# Compile all Java files
javac -cp ".;mysql-connector-j-9.3.0.jar" Server.java Headquarter.java Camp.java
```

### **Execution Order**

#### **Step 1: Start the Server**
```bash
java -cp ".;mysql-connector-j-9.3.0.jar" Server
```
**Expected Output:**
```
Disaster Resource Management Server Starting...
Database connected successfully!
Server listening on port 12345
```

#### **Step 2: Start Headquarters**
```bash
java -cp ".;mysql-connector-j-9.3.0.jar" Headquarter
```
**Expected Output:**
```
Connecting to Disaster Management Server...
✓ Headquarters registered successfully!
=== HEADQUARTERS MENU ===
1. View Active Camp Sites
2. View All Resource Requests
3. View All Logs
4. Approve/Reject Request
5. Exit
```

#### **Step 3: Start Camp Clients**
```bash
java -cp ".;mysql-connector-j-9.3.0.jar" Camp
```
**Expected Output:**
```
Connecting to Disaster Management Server...
Enter camp name: [Enter camp name]
Successfully registered as Camp [Number] - [Camp Name]
=== CAMP SITE MENU ===
1. Send Resource Request to HQ
2. View Available Resources
3. View Request Logs
4. Exit
```

### **Testing Workflow**
1. Start **Server**
2. Start **Headquarters**
3. Start multiple **Camp** instances
4. From Camp: Send resource request
5. From HQ: View and approve/reject requests
6. Monitor real-time updates

## 🔧 Implementation Details

### **Core Java Files**

#### **1. Server.java**
**Purpose**: Central server handling all client connections
**Key Features**:
- Multi-threaded client handling
- Database connection management
- Message routing between clients
- Resource allocation logic
- Logging and audit trails

**Important Methods**:
- `initializeDatabase()`: Establishes MySQL connection
- `registerCamp()`: Registers new camps
- `sendToHQ()`: Routes messages to headquarters
- `sendToCamp()`: Routes messages to specific camp

#### **2. Camp.java**
**Purpose**: Field camp client application
**Key Features**:
- Menu-driven text interface
- Resource request generation
- Real-time status updates
- Automatic reconnection handling

**Menu Options**:
1. Send Resource Request to HQ
2. View Available Resources
3. View Request Logs
4. Exit

#### **3. Headquarter.java**
**Purpose**: Headquarters client application
**Key Features**:
- Real-time request monitoring
- Approval/Rejection system
- Comprehensive logging
- Active camp tracking

**Menu Options**:
1. View Active Camp Sites
2. View All Resource Requests
3. View All Logs
4. Approve/Reject Request
5. Exit

### **Communication Protocol**
Client-Server messages use pipe-separated format:
```
COMMAND|param1|param2|param3
```

**Example Commands**:
- `REGISTER_CAMP|CampName`
- `SEND_REQUEST|Water|100|3`
- `APPROVE_REQUEST|5`
- `GET_LOGS|0`

## 🔄 Workflow

### **Camp Registration Flow**
```
1. Camp connects to Server (port 12345)
2. Camp sends REGISTER_CAMP with camp name
3. Server generates unique camp number
4. Server assigns initial resources
5. Camp receives registration confirmation
6. Camp appears in HQ's active camps list
```

### **Resource Request Flow**
```
1. Camp selects "Send Resource Request"
2. Camp enters: Resource, Amount, Deadline
3. Request saved to database (PENDING)
4. HQ receives real-time notification
5. HQ views request and chooses Approve/Reject
6. If Approved: Resources added to camp inventory
7. If Rejected: Camp notified with reason
8. Status updated in database
9. Log entry created
```

### **Initial Resource Allocation**
Each new camp receives:
- Water: 100 liters
- Food: 50 kgs
- Medicines: 20 boxes
- Blankets: 30 pieces
- Tents: 5 units
- First Aid Kits: 10 kits

## 📁 Project Structure
```
JavaProject/
├── README.md                    # This file
├── Server.java                  # Main server application
├── Headquarter.java            # Headquarters client
├── Camp.java                   # Field camp client
├── Database.sql                # MySQL database schema
├── test.txt                    # Compilation and execution commands
├── mysql-connector-j-9.3.0.jar # MySQL JDBC driver
├── idea_report_java.pdf        # Project idea report
├── Case_Study_java.pdf         # Disaster management case study
└── final_report.docx           # Complete project documentation
```

## 🚧 Challenges Faced

### **Technical Challenges**

1. **Concurrent Client Management**
   - Challenge: Handling multiple simultaneous connections
   - Solution: Implemented thread-safe `ConcurrentHashMap` and synchronized methods

2. **Database Connection Pooling**
   - Challenge: Managing multiple database connections efficiently
   - Solution: Shared static connection with synchronized access

3. **Real-time Notification System**
   - Challenge: Immediate updates between HQ and Camps
   - Solution: Event-driven messaging with observer pattern

4. **Thread Synchronization**
   - Challenge: Preventing race conditions in shared resources
   - Solution: Used `synchronized` blocks and concurrent collections

5. **Network Reliability**
   - Challenge: Handling client disconnections gracefully
   - Solution: Implemented heartbeat mechanism and cleanup procedures

### **Development Challenges**

1. **Protocol Design**
   - Challenge: Creating efficient client-server communication protocol
   - Solution: Designed simple pipe-separated command format

2. **Error Handling**
   - Challenge: Robust error recovery across distributed system
   - Solution: Comprehensive try-catch blocks with logging

3. **Testing Distributed System**
   - Challenge: Simulating multiple clients and edge cases
   - Solution: Created test scripts and manual testing procedures

## 🔮 Future Enhancements

### **Immediate Improvements**

1. **Security Enhancements**
   - User authentication with passwords
   - SSL/TLS encryption for network communication
   - Role-based access control

2. **Advanced Features**
   - Automatic resource reordering based on consumption patterns
   - Predictive analytics for resource needs
   - GIS integration for camp location mapping
   - Mobile application for field workers

3. **Performance Optimizations**
   - Database connection pooling
   - Caching frequently accessed data
   - Asynchronous message processing
   - Load balancing for multiple servers

4. **User Interface**
   - Graphical User Interface (GUI) using JavaFX/Swing
   - Web-based dashboard
   - Real-time data visualization charts
   - Mobile-responsive design

### **Scalability Features**

1. **Cloud Deployment**
   - Docker containerization
   - Kubernetes orchestration
   - AWS/Azure cloud deployment
   - Auto-scaling based on demand

2. **Integration Capabilities**
   - REST API for third-party integration
   - SMS/Email notification system
   - Integration with government disaster management systems
   - IoT device integration for real-time monitoring

3. **Advanced Analytics**
   - Machine learning for resource prediction
   - Disaster impact assessment tools
   - Evacuation route optimization
   - Resource allocation algorithms

## 📚 References

### **Academic Resources**
1. **Object-Oriented Programming Concepts**
   - Java Documentation: https://docs.oracle.com/javase/8/docs/
   - Java Networking: https://docs.oracle.com/javase/tutorial/networking/

2. **Database Design**
   - MySQL Documentation: https://dev.mysql.com/doc/
   - JDBC Tutorial: https://docs.oracle.com/javase/tutorial/jdbc/

3. **Disaster Management**
   - National Disaster Management Guidelines, India
   - UN Office for Disaster Risk Reduction

### **Technical Documentation**
1. **Java Sockets**
   - Oracle Java SE Documentation
   - Java Network Programming by Elliotte Rusty Harold

2. **Multi-threading**
   - Java Concurrency in Practice by Brian Goetz
   - Oracle Java Concurrency Tutorial

3. **Project Methodology**
   - Software Engineering Body of Knowledge (SWEBOK)
   - Agile Development Principles

### **Case Studies Referenced**
1. **2013 Kedarnath Floods, Uttarakhand**
   - Disaster response analysis
   - Resource coordination challenges

2. **Perennial Floods of Bihar**
   - Annual disaster management requirements
   - Large-scale resource distribution challenges

---

<div align="center">

## 🏆 Project Information

**Course**: Object Oriented Programming using JAVA (CS032003)  
**Semester**: 3rd Semester MCA (AI & IoT)  
**Institution**: National Institute of Technology Patna  
**Supervisor**: Dr. Anand Shanker Tewari  
**Duration**: July 2025 – December 2025

## 🌟 Star this repository if you found it useful!

[![GitHub stars](https://img.shields.io/github/stars/prashant-mishra-22/JavaProject?style=for-the-badge&logo=github)](https://github.com/prashant-mishra-22/JavaProject/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/prashant-mishra-22/JavaProject?style=for-the-badge&logo=github)](https://github.com/prashant-mishra-22/JavaProject/network/members)
[![GitHub issues](https://img.shields.io/github/issues/prashant-mishra-22/JavaProject?style=for-the-badge&logo=github)](https://github.com/prashant-mishra-22/JavaProject/issues)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **NIT Patna** for providing academic environment and resources
- **Dr. Anand Shanker Tewari** for guidance and supervision
- **Team Members** for collaborative development effort
- **Open Source Community** for tools and libraries

## 🐛 Bug Reports & Contributions

Found a bug? Have a feature request? Please open an issue on GitHub or submit a pull request. Contributions are welcome!

**Made with ❤️ by Team DRMS | NIT Patna**

[Rishi Kumar](https://github.com/rishikr507) • 
[Prashant Kumar Mishra](https://github.com/prashant-mishra-22) • 
[Satyam Bhardwaj](https://github.com/ijugunu) • 
Mayank Shaw • 
Monil Mishra • 
Biswajit Ghadei

</div>
