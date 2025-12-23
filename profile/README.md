# SproutVR

**Capstone Project - FPT University**

* **Project Code:** FA25SE198
* **Group Code:** GFA25SE07

## Introduction

**SproutVR** is an EduTech platform designed to bridge the gap between immersive virtual reality learning and real-time classroom management. The system addresses the challenge of limited interactivity in traditional classrooms by allowing students to engage with 3D simulations while enabling instructors to monitor, assist, and grade progress instantly.

The solution consists of three main components:

1. **Provider System (Web):** A marketplace and management hub for organizations to purchase maps and manage licenses.


2. **School System (Desktop):** A local server and management app for teachers to create lessons, manage VR devices, and monitor sessions via LAN.


3. **Game (VR Client):** An immersive application for students to perform tasks and interact with learning content.



## Database Design

The system utilizes a relational database structure to manage users, licenses, and learning content.

**Provider System ERD:** Handles Organizations, Orders, Maps, and License Keys.

![SproutVR Provider System Logical ERD](doc/images/provider/erd/figure67.png)

**School System ERD:** Handles Teachers, Students, VR Devices, and Session Results.

![SproutVR School System Logical ERD](doc/images/school/erd/figure68.png)

## Game (VR Client)

The VR client is designed for the **Meta Quest 3**, providing high-fidelity interaction and real-time synchronization with the teacher's dashboard.

### Tech Stacks

| Category | Technology | Purpose |
| --- | --- | --- |
| **Engine** | **Unity 6000.2.8f1** | Core 3D development platform. |
| **XR Framework** | **OpenXR / XR Interaction Toolkit** | Cross-platform VR interaction handling.|
| **Networking** | **gRPC Client** | High-performance real-time communication with the backend.|
| **DI Container** | **Extenject (Zenject)** | Dependency injection for modular code architecture.|
| **Assets** | **DoTween / ModernUI** | UI animations and pre-built components.|

## Provider (Web System)

The Provider System serves as the central hub for distributing content to schools (Organizations) and managing subscriptions.

### Tech Stacks

| Category | Technology |
| --- | --- |
| **Frontend** | React 19, Vite, TailwindCSS, ShadCN UI.|
| **Backend** | ASP.NET Core Web API (.NET 9).|
| **Database** | PostgreSQL, Redis (Caching).|
| **Architecture** | Microservices with YARP API Gateway.|
| **Payment** | PayOS Integration.|

### Use Case Diagrams

![Use Case Diagram for SproutVR Provider System](doc/images/provider/usecase/figure02.png)

### Architecture Diagram

![Architecture Diagram for SproutVR Provider System](doc/images/provider/architecture/figure72.png)


### Screen Flow

![Provider System Screen Flow - Guest](doc/images/provider/screenflow/figure12.png)

![Provider System Screen Flow - Organization](doc/images/provider/screenflow/figure13.png)

![Provider System Screen Flow - System Admin](doc/images/provider/screenflow/figure14.png)


## School (Desktop System)

The School System is a local desktop application that acts as the "Local Server" for the classroom. It connects to VR headsets via a Wi-Fi Hotspot (LAN) to ensure low latency.

### Tech Stacks

| Category | Technology |
| --- | --- |
| **Desktop Shell** | <br>**Electron 38** (Cross-platform desktop framework).|
| **Frontend** | React 19, Vite, Redux Toolkit.|
| **Backend (Local)** | ASP.NET Core (.NET 9), gRPC Server.|
| **Real-time** | <br>**Redis Streams** (For syncing headset movements/tasks).|
| **Database** | PostgreSQL (Local Instance).|
| **AI** | OpenAI / Gemini Integration (AI Assistant).|

### Use Case Diagrams

![Use Case Diagram for SproutVR School System](doc/images/school/usecase/figure07.png)

### Architecture Diagram

![Architecture Diagram for SproutVR School System](doc/images/school/architecture/figure73.png)

### Screen Flow

![School System Screen Flow - Teacher](doc/images/school/screenflow/figure15.png)

![School System Screen Flow - School Admin](doc/images/school/screenflow/figure16.png)

## Team Members & Supervisors

**Group GFA25SE07**

| Name | Role | Student ID |
| --- | --- | --- |
| **Vũ Kim Duy** | Team Leader | SE182407 |
| **Cao Ngô Phương Khánh** | Member | SE181509 |
| **Lê Quang Khánh** | Member | SE182420 |
| **Nguyễn Gia Bảo Anh** | Member | SE183425 |
| **Võ Thị Mai Hoa** | Member | SE183659 |

**Supervisors:**

* Lâm Hữu Khánh Phương
* Lý Ánh Dương
