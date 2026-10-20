# Enterprise n8n & Python Data Transformation Pipeline

A production-ready asynchronous data orchestration pipeline built with **n8n** and native **Python**, designed to process incoming webhook events, perform schema transformation, and return structured responses in real time.

---

## 🚀 Architecture Overview

1. **Webhook Trigger (Ingestion):** Receives structured JSON payloads securely over HTTPS (`POST /webhook/ingest-data`).
2. **Python Transformation Node:** Sanitizes, normalizes, and applies business transformation logic to incoming fields natively without third-party dependencies.
3. **Webhook Response Node:** Emits immediate status confirmation (`pipeline_status: SUCCESS`) alongside transformed payloads for downstream CRM/Database consumption.

---

## 🛠️ Tech Stack

* **Orchestration:** n8n (Cloud/Self-hosted)
* **Transformation Logic:** Python 3 (Native Engine)
* **Interface:** RESTful Webhooks
* **Deployment & Testing:** Linux Terminal / Curl / Termux

---

## 📥 Sample Request & Response

### Request Payload:
```json
{
  "project": "AI Pipeline",
  "status": "active"
}
 
