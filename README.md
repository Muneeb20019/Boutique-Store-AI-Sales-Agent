# 🤖 Intelligent Agent Hub: Boutique Concierge Assistant

**[🌐 Live Chat Demo](https://sales-ai-agent-n8n-ajy3.vercel.app/) | [🎥 Video Demonstration](PASTE_YOUR_VIDEO_LINK_HERE)**

---

## 🖼️ System Architecture & UI Preview

| n8n Logic Engine (Backend) | Premium Boutique UI (Frontend) |
| :---: | :---: |
| <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/workflow_screenshot.png" width="450" alt="n8n Workflow"/> | <img src="https://github.com/Muneeb20019/Sales-AI-Agent-n8n/raw/main/frontend_screenshot.png" width="400" alt="Frontend UI"/> |

*Note: Please upload your screenshots to the repository and update the image paths above to see them in the README.*

---

## 🚀 Project Overview
Developed for a high-end **Boutique Digital Agency**, this system functions as an intelligent digital concierge. It manages the full client lifecycle from **Autonomous Discovery (Phase 1)** to **Human Escalation (Phase 2)**. 

The system leverages **Retrieval-Augmented Generation (RAG)** to provide accurate agency information and features a real-time bridge to **Discord** for seamless staff takeover.

## 🧠 Core Technical Pillars

### 1. RAG-Powered Knowledge Retrieval
The agent utilizes a **Supabase Vector Store** powered by **Gemini Embeddings**. By processing a company PDF knowledge base into 768-dimensional vectors, the bot provides authoritative answers regarding agency history, expertise, and services without hallucinations.

### 2. State-Driven Logic (The Phase Gate)
Using **Supabase** as a persistent state-layer, the workflow tracks user progression. 
- **Discovery Mode:** The AI proactively collects 5 critical data points (Project Type, Brand, Industry, Budget, Timeline).
- **Escalation Mode:** Once contact info is provided, the system automatically transitions from the AI brain to business-hour logic.

### 3. Time-Aware Routing (CET Logic)
Custom **JavaScript** logic validates the current time in **Milan, Italy (CET)** to manage agency expectations.
- **Inside Hours (9 AM - 6 PM CET):** Initiates a live human handoff alert via Discord.
- **Outside Hours:** Sets automated email follow-up expectations and logs details for the next business day.

### 4. Universal Intent Engine
To ensure a "human-centric" experience, I built a universal keyword matching engine. This allows the system to detect escalation requests (e.g., "talk," "representative," "1," "help") regardless of how the user phrases the request.

## ✨ Advanced Features (Python Integrated)
- **🐍 Python Data Transformation:** Utilized custom **Python nodes** within n8n to perform complex data merging. This cleanses and standardizes the AI response and business templates into a single, clean JSON schema for the frontend.
- **🛡️ Collision Prevention:** Implemented a state-locking mechanism that pauses the AI Agent once a human handoff is active, ensuring a professional one-on-one conversation.
- **🎨 Premium Frontend:** A high-performance **Vanilla JavaScript** application hosted on **Vercel**, featuring glassmorphism aesthetics and animated mesh gradients to reflect a boutique brand identity.

## 🚀 Technical Stack
| Layer | Technology |
| :--- | :--- |
| **Automation** | n8n Orchestration |
| **AI Brain** | Google Gemini-1.5-Flash |
| **Vector DB** | Supabase (pgvector) |
| **Backend Code** | **Python** & JavaScript |
| **Frontend** | Vanilla JS / CSS3 (Deployed via Vercel) |
| **Escalation** | Discord API & Webhooks |

---

## 🛠️ How to Use
1.  Open the **[Live Demo](https://sales-ai-agent-n8n-ajy3.vercel.app/)**.
2.  Inquire about agency history or expertise (Retrieval Test).
3.  Provide an email address to trigger the **Phase 2** logic.
4.  Request a human (e.g., "I want to talk to someone") to trigger the **Discord Escalation**.

---

## ✍️ Author
**Muneeb Ali Khan**
- **GitHub:** [@Muneeb20019](https://github.com/Muneeb20019)
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)
