# 🏦 Bank-Management-System-Simulation-Project

This project simulates a real-world **Bank Management System** using **Arena Simulation Software**. It models customer arrivals, service routing, queuing, and resource usage for key banking operations such as **Account Opening**, **ATM Transactions**, **Deposits**, and **Billing**. The simulation aims to analyze system performance and identify optimization opportunities.

---

## 🎯 Objective

To design a discrete-event simulation of a bank using Arena that evaluates service flow efficiency, queue behavior, and resource utilization to improve customer satisfaction and operational management.

---

## ⚙️ Features

- Randomized customer arrivals
- Probabilistic assignment of service types using `DISC`
- Routing based on `Customer.Type` via N-Way by Condition
- Queuing and resource allocation at each service station
- Centralized station-based exit for clean reporting
- Record modules for tracking service metrics
- Multiple replications for performance validation

---

## 🧩 Arena Modules Used

| Module      | Role                                          |
|-------------|-----------------------------------------------|
| Create      | Generate customer entities                    |
| Assign      | Assign `Customer.Type` using `DISC` function  |
| Decide      | Route entities to services (N-Way Condition)  |
| Process     | Simulate service with queue + resource        |
| Resource    | Represent staff or ATM machine                |
| Record      | Log queue time and service count              |
| Route       | Send customers to central exit station        |
| Station     | Central exit point for all service paths      |
| Dispose     | Remove customers from the system              |

---

## 🔄 Customer Type Mapping

| `Customer.Type` | Service Type     |
|------------------|------------------|
| 1                | Account Opening  |
| 2                | ATM              |
| 3                | Deposit          |
| 4                | Billing          |

---

## 🖥️ Software Requirements

- **Arena Simulation Software** (Rockwell Automation, v14 or later)
- Optional: MS Word / Excel for documentation and analysis

---

## 📊 Output & Analysis

- Service count per module
- Time in queue (per path)
- Resource utilization rates
- Centralized exit reporting

---

## 📁 Project Structure

```plaintext
📁 Bank-Management-System-Simulation-Project
│
├── README.md
├── Bank_Simulation.doe         # Arena model file
├── Final_Report.docx           # Complete project report
├── QueueStats.xlsx (optional)  # Exported statistics
