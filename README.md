# 🕵️‍♂️ Kusto Detective Agency Lab

This project demonstrates applied **Kusto Query Language (KQL)** expertise within **Azure Data Explorer**, inspired by Microsoft’s *Kusto Detective Agency* challenge.

---

## 🧠 Overview
Building on my prior experience with **Microsoft Sentinel** and **KQL**, I conducted advanced log analysis to simulate **SOC-style investigations**.  
By summarizing, filtering, and visualizing telemetry data, I strengthened my approach to **threat detection** and **analytics rule design** in cloud environments.

---

## 🧩 Key Focus Areas
- SOC event investigation and data summarization using **KQL**  
- Hands-on query execution in **Azure Data Explorer**  
- Query optimization and result visualization for **Sentinel integration**  
- Laying groundwork for **custom analytics rule development**

---

## 📊 Hands-on Queries

### 🔹 Create and Ingest Data
```kql
.create table DetectiveCases(
    Timestamp:datetime,
    EventType:string,
    DetectiveId:string,
    CaseId:string,
    Properties:dynamic
)
.ingest async into table DetectiveCases ('https://kustodetectiveagency.blob.core.windows.net/kda2start/log_00000.csv.gz')
.ingest async into table DetectiveCases ('https://kustodetectiveagency.blob.core.windows.net/kda2start/log_00001.csv.gz')
.ingest into table DetectiveCases ('https://kustodetectiveagency.blob.core.windows.net/kda2start/log_00002.csv.gz')
