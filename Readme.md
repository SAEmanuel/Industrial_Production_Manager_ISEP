<div align="center">

  # 🏭 Industrial Production Manager
  ### Smart Factory Solution

  <p align="center">
    An integrated system for <b>Production Planning</b>, <b>Shop Floor Simulation</b>, and <b>Machine Control</b> designed for short-run and project-based manufacturing.
  </p>

  <p align="center">
    <a href="https://skillicons.dev">
      <img src="https://skillicons.dev/icons?i=java,c,mysql,maven,idea,git,linux&theme=dark" />
    </a>
  </p>

  ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
  ![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
  ![Assembly](https://img.shields.io/badge/Assembly-Run_Low_Level-525252?style=for-the-badge&logo=cpu&logoColor=white)
  ![PL/SQL](https://img.shields.io/badge/PL%2FSQL-Oracle_DB-F80000?style=for-the-badge&logo=oracle&logoColor=white)

</div>

---

## 📘 Project Overview

Developed within the scope of the **Integrative Project (3rd Semester - LEI/ISEP)**, this solution addresses the needs of **KeepIt Simple Solutions (KS)**, focusing on the management of flexible industrial units.

The system is composed of multiple interacting modules that handle everything from high-level project management (using **PERT/CPM**) to low-level hardware control of factory machines (using **C/Assembly** on Raspberry Pi).

---

## ⚙️ System Architecture & Modules

The solution is divided into four main applications:

### 1. 🏗️ Plant Floor Advanced Tools (Java)
* **Production Simulation:** Simulates the processing of items through workstations based on priority queues and machine availability.
* **Project Manager:** Implements **PERT/CPM (Critical Path Method)** to analyze project schedules, detect bottlenecks, and calculate slack times using **Graph Theory**.
* **Data Structures:** Utilizes **BST/AVL Trees** for material management and **Heaps** for priority-based quality checks.

### 2. 🤖 Machine Supervisor (C & Assembly)
* **Low-Level Control:** Developed to run on **Raspberry Pi**.
* **Sensor Integration:** Reads temperature and humidity sensors to monitor machine health.
* **Actuators:** Controls LEDs to signal machine status (Operation/Idle/Off) and binary operation codes.
* **Safety Mechanisms:** Implements "Moving Median" filters to detect sensor anomalies and trigger alerts.

### 3. 🗄️ Database Management (PL/SQL)
* **Persistence:** Oracle Database storing Products (BOM), Operations (BOO), Orders, and Stock.
* **Logic:** Uses complex **Triggers** and **Stored Procedures** to validate business rules (e.g., preventing circular dependencies in BOMs, checking stock availability).

### 4. 🏭 Plant Floor Manager (Java/UI)
* **Coordination:** Bridges the gap between the high-level planning tools and the low-level machine data.
* **Visualization:** Imports and visualizes the Bill of Materials (BOM) and Bill of Operations (BOO).

---

## 🚀 Build & Run

This project uses **Maven** for the Java components. Ensure you have JDK 11+ and an Oracle Database connection configured.

### 📦 Core Commands

| Action | Command |
| :--- | :--- |
| **Run Unit Tests** | `mvn clean test` |
| **Build JAR** | `mvn package` |
| **Run App** | `java -jar target/project-template-1.0-SNAPSHOT-jar-with-dependencies.jar` |

### 🔍 Quality & Coverage

<details>
<summary>Click to see advanced analysis commands</summary>

#### Documentation
```bash
mvn javadoc:javadoc
