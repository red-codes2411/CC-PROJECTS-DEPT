# CC-PROJECTS-DEPT
Cloud based server for district level - based off the problem statement

# EduBridge Hub – AWS Deployment Overview

This project sets up a cloud-based hub to store, sync, and distribute educational content using AWS services.

## 🚀 Infrastructure Setup

### 1. File Storage

* **Service:** Amazon S3
* Created bucket `edubridge-hub-content-YOURNAME` (Mumbai)
* Stores videos, PDFs, and lesson content

### 2. Database

* **Service:** Amazon RDS (PostgreSQL)
* Database: `edubridge-hub-db`
* Stores users, logs, sync history, and node data

### 3. Cache & Scheduler

* **Service:** Upstash Redis
* Used for caching and running background sync jobs (Celery)

### 4. Permissions

* **Service:** Amazon IAM
* Configured secure role-based access (no hardcoded credentials)

### 5. Server Deployment

* **Service:** AWS Elastic Beanstalk (EC2 t3.micro)
* Live Flask server deployed and publicly accessible

### 6. Database Connectivity

* **Service:** AWS Security Groups
* Opened port `5432` to allow server ↔ database communication

---

## 🔧 Pending Tasks

### 7. Deploy Hub Backend

* Replace Flask demo with FastAPI EduBridge hub

### 8. Initialize Database

* Run schema SQL to create required tables

### 9. Configure Cloud Connection

* Add API URL and auth token via environment variables

### 10. Test Content Sync

* Verify flow: Cloud → Hub → S3 → Database logging

### 11. Connect School Node

* Register node using hub public URL (port 8000)
* Ensure offline-capable content access

---

## 🧩 Tech Stack

* AWS S3, RDS, IAM, Elastic Beanstalk
* PostgreSQL
* Redis (Upstash)
* FastAPI (planned)

---

If you want, I can also make this look more *resume/project submission level polished* or add architecture diagrams 👀

