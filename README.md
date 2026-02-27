# 🚨 TRACEGUARD – Cross-Channel Mule Account Detection System

## 📌 Project Overview

TRACEGUARD is a real-time AI-powered fraud detection system designed to detect and prevent **money mule accounts** across multiple banking channels.

The system builds a **unified entity graph** from cross-channel transaction data and applies a **Graph Neural Network (GNN)** to detect coordinated mule rings, suspicious velocity patterns, and hidden fraud networks — all in under 500 milliseconds.

This project demonstrates how graph intelligence + real-time streaming can solve modern financial fraud problems that traditional rule-based systems cannot detect.

---

## 🎯 Objectives

* Eliminate fraud detection silos across banking channels
* Detect mule rings using graph-based intelligence
* Score accounts in real-time before cash-out
* Automatically block high-risk accounts
* Provide explainable AI decisions for analysts

---

## 🏗️ System Architecture (High-Level)

The system follows a 5-layer event-driven architecture:

1️⃣ Data Sources Layer
2️⃣ Streaming & Processing Layer
3️⃣ Entity Graph Layer
4️⃣ GNN Scoring Layer
5️⃣ Action & Alert Layer

Data flows from transaction channels → streaming engine → graph update → GNN scoring → automated decision.

---

## 🧩 Core Components

### 1. Multi-Channel Ingestion

Collects transaction and login events from:

* Mobile App
* Web Portal
* UPI / IMPS
* ATM Network
* Wallet APIs
* Core Banking System

### 2. Entity Resolution Engine

Unifies identities across channels:

* Account
* Device
* IP Address
* Phone Number
* Beneficiary

### 3. Dynamic Knowledge Graph

Stores all entities and relationships in a live graph database.

Nodes:

* Accounts
* Devices
* IPs
* Phones
* Beneficiaries

Edges:

* Transfers
* Logins
* Device sharing
* Account relationships

### 4. Graph Neural Network (GraphSAGE)

* Learns multi-hop fraud patterns
* Detects mule rings
* Produces risk score (0–1)
* Works for new accounts (inductive learning)

### 5. Decision & Action Engine

* Monitor low-risk accounts
* Flag suspicious accounts
* Restrict high-risk accounts
* Auto-block confirmed mule accounts

---

## 📂 Project Structure

```
TRACEGUARD/
│
├── data/                     # Sample transaction datasets
├── ingestion/                # Kafka producers & event normalizers
├── entity_resolution/        # Identity unification logic
├── graph_engine/             # Graph creation & update logic
├── feature_engineering/      # Velocity & behavioral feature extraction
├── gnn_model/                # GraphSAGE model training & inference
├── scoring_engine/           # Risk scoring pipeline
├── action_engine/            # Blocking & alert logic
├── dashboard/                # Analyst monitoring UI (if applicable)
├── configs/                  # Configuration files
├── notebooks/                # Experiments & model research
└── README.md                 # Project documentation
```

---

## ⚙️ How It Works (Execution Flow)

1. Transaction event is generated
2. Event is streamed through Kafka
3. Identity resolution links entities
4. Graph database updates relationships
5. Feature extraction runs on subgraph
6. GNN model generates risk score
7. Decision engine triggers action

Total detection time: < 500 ms

---

## 🛠️ Technology Stack

* Apache Kafka – Event streaming
* Apache Flink – Stream processing
* Neo4j – Graph database
* Redis – Velocity & caching layer
* PyTorch Geometric – Graph Neural Network
* Triton – Model serving
* Kubernetes – Scalable deployment

---

## 📊 Expected Outcomes

* High mule ring detection accuracy
* Very low false positive rate
* Real-time fraud prevention
* Full audit trail for compliance
* Scalable to millions of transactions per second

---

## 🚀 Future Enhancements

* Federated learning across banks
* Advanced community detection algorithms
* Real-time anomaly visualization dashboard
* Adaptive model retraining pipeline

---

## 👥 Team

TRACEGUARD
Detect · Protect · Prevent
