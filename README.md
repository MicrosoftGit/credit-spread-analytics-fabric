# credit-spread-analytics-fabric
## 📊 Credit Spread Analytics Demo with Microsoft Fabric

This repository contains a **demo implementation of credit spread analytics** built using **Microsoft Fabric**, **Fabric IQ (Copilot)**, and **Power BI**.

The goal is to demonstrate how Fabric enables **end‑to‑end analytics** — from raw market data to explainable insights — and how the same foundation can be reused across **Risk IQ, Portfolio IQ, and Research IQ** scenarios.

***

## 🚀 Demo Overview

Today, credit spreads are widening, signaling increased risk in our corporate loan portfolio. We need to identify, at a glance, which sectors are deteriorating and proactively mitigate exposure. The goal of this demo is to move from "raw data" to "unified intelligence," showcasing how Fabric IQ turns data into actionable business meaning. 

The demo showcases:

*   Credit spread curves by **rating, sector, and tenor**
*   Historical spread widening / tightening analysis
*   Decomposition of spread drivers (rates vs credit)
*   Natural‑language explanations using **Fabric IQ / Copilot**
*   A reusable Lakehouse foundation for other IQ offerings

Fabric gives us 360-degree visibility, reduced compliance risk, and faster decision-making. And, Fabric IQ allows us to model our business using natural language, not complex SQL schemas.

This is a **demo and reference implementation**, not a production system.

***

## 🧱 Architecture

**Core services used:**

*   **Microsoft Fabric**
    *   OneLake
    *   Lakehouse
    *   Fabric Data Engineering
    *   Fabric Data Science
*   **Power BI (Direct Lake)**
*   **Fabric IQ (Copilot in Fabric)**

High‑level flow:

    Market Data → OneLake → Lakehouse
                              ↓
                      Data Engineering
                              ↓
                      Power BI (Direct Lake)
                              ↓
                     Fabric IQ / Copilot

📌 Detailed architecture diagrams live in `/architecture`.

***

## 📁 Repository Structure

| Folder          | Description                                              |
| --------------- | -------------------------------------------------------- |
| `data/`         | Sample datasets and schema documentation                 |
| `notebooks/`    | Fabric notebooks for ingestion, transformation, analysis |
| `powerbi/`      | Power BI report assets                                   |
| `architecture/` | Architecture diagrams                                    |
| `scripts/`      | Jumpstart install notes and setup helpers                |

***

## 🧪 Data Model (High Level)

**Bronze**

*   Raw credit spread data
*   Yield curves
*   Reference data (rating, sector)

**Silver**

*   Normalized instruments
*   Aligned tenors
*   Standardized spread metrics

**Gold**

*   Aggregated spreads (IG vs HY)
*   Sector and rating rollups
*   Spread deltas and trend indicators

This structure aligns with **Materialized Lake Views** in Fabric.

***

## 🤖 Fabric IQ / Copilot Examples

Example prompts enabled by this demo:

*   *“Why did BBB industrial credit spreads widen in Q3?”*
*   *“Compare IG and HY spread volatility over the last year.”*
*   *“Which sectors contributed most to spread widening?”*

All responses are grounded in **OneLake data**.

***

## ⚙️ Getting Started (Demo Setup)

### Prerequisites

*   Microsoft Fabric workspace
*   Fabric capacity (Trial or SKU)
*   Power BI enabled

### Recommended Jumpstarts

*   **Getting Started with Fabric Jumpstart**
*   **Getting Started with Materialized Lake Views**
*   **Any Core Power BI demo**

Installation instructions are in `/scripts/install_jumpstarts.md`.

***

## ⚠️ Notes & Limitations

*   This demo uses **sample or synthetic data**
*   Dependency warnings in Fabric notebooks are expected and safe to ignore
*   Not intended for regulated or production workloads

***

## 🔮 Future Enhancements

*   Spread shock detection (anomaly detection)
*   Scenario analysis & stress testing
*   Portfolio‑level exposure rollups
*   Integration with Copilot Studio agents

***

## 📄 License

This project is provided for **demo and educational purposes only**.

***

# 4️⃣ Create the Repo in GitHub (5 Minutes)

### Option A: GitHub UI (Fastest)

1.  Go to **<https://github.com/new>**
2.  Repo name: `fabric-credit-spread-demo`
3.  Description:
    > End-to-end credit spread analytics demo using Microsoft Fabric and Fabric IQ
4.  ✅ Public (recommended for demos)
5.  ✅ Add README
6.  Click **Create repository**
7.  Replace README with the content above

***

### Option B: Local Git (If You Prefer)

```bash
git init fabric-credit-spread-demo
cd fabric-credit-spread-demo
git remote add origin https://github.com/<your-username>/fabric-credit-spread-demo.git
```

Add files, then:

```bash
git add .
git commit -m "Initial credit spread demo structure"
git push -u origin main
```

***

