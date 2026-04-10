# Elevator Management System — ER Design

This repository contains the **Entity Relationship (ER) Design** and **Database Schema** for a comprehensive **Elevator Management System**.  
The goal is to model a real-world system that manages elevators across multiple buildings, floors, and shafts — tracking requests, trips, status, emergencies, and maintenance.

---
dbDigram link 
https://dbdiagram.io/d/elevator-69d8dc620f7c9ef2c0c708f2

## 🧠 Overview

Elevators are an essential part of modern buildings. This project defines a **scalable database structure** to support:

- Multi-system & multi-building deployments
- Floor-level requests
- In-cabin requests
- Emergency handling
- Trip tracking
- Maintenance logging
- Real-time elevator status tracking

The schema is built using **DBML** with clear relationships, enums, timestamps, and appropriate constraints.

---

## 📌 Features

✔ Multi-system support  
✔ One-to-many building & floors relationships  
✔ One-to-one elevator ↔ shaft mapping  
✔ External (floor) and internal (cabin) elevator requests  
✔ Emergency logs for overload, fire, technical errors  
✔ Passenger trip tracking  
✔ Elevator status logs  
✔ Maintenance records

---

## 🗂️ Database Tables

The following tables are included:

| Table Name       | Description |
|------------------|-------------|
| `system`         | Root entity for elevator system |
| `building`       | Stores building info |
| `floor`          | Floor details of a building |
| `elevatorShaft`  | Elevator shaft structure |
| `elevator`       | Elevator unit details |
| `floorReq`       | External floor button calls |
| `elevatorReq`    | Internal elevator button requests |
| `emergencyLog`   | Emergency events log |
| `trip`           | Elevator trip history |
| `elevatorStatus` | Real-time elevator statuses |
| `maintenance`    | Elevator maintenance logs |

---

## 🔗 Relationships

- One **system** can have many **buildings**
- One **building** can have many **floors** and **shafts**
- One **shaft** is assigned to one **elevator**
- One **elevator** can have:
  - Many floor requests
  - Many internal elevator requests
  - Many emergency logs
  - Many trip logs
  - Many status logs
  - Many maintenance records

---

## 📁 Folder Structure

Your project should be structured like:
