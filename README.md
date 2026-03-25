🧵 AI Compliance Auditor & Digital Product Passport (DPP) Generator
Bridging Karachi’s Textile Industry to EU 2027 Regulations
📌 Project Overview
As the European Union moves toward mandatory Digital Product Passports (DPP) by 2027 under the Ecodesign for Sustainable Products Regulation (ESPR), global exporters face a massive documentation challenge.

This project is an End-to-End AI Compliance Terminal developed on a Dell Latitude 5490 (16GB RAM). It automates the verification of textile garments—from physical label scanning to regulatory cross-referencing—ensuring that exports from Port Qasim meet international "Green" and "Trade" standards.

🚀 Key Features
Multimodal Visual Audit: Uses Computer Vision to extract material composition and care instructions directly from garment labels.

Local Legal RAG: A high-performance FAISS Vector Database containing EU Trade Clauses, allowing for "Privacy-First" legal querying.

Agentic Self-Correction: An AI Agent capable of "Tool Use" to verify real-time GSP+ Tax Status and Port Qasim-to-EU Shipping Rates via simulated SQL/API calls.

DPP Generator: Automatically synthesizes audit findings into a standardized JSON-LD format and generates a scannable QR Code for industrial hang-tags.

🛠️ Technical Stack
Core AI: Google Gemini 2.0 Flash (Vision & Reasoning)

Vector Engine: FAISS (Facebook AI Similarity Search)

Data Handling: Pydantic v2 (Validation), JSON-LD (Standardization)

Tools: OpenCV (Imaging), Python-QRCode, Google GenAI SDK

📂 Project Structure
Bash
├── data/
│   ├── eu_regulations_index/   # FAISS Vector Index
│   └── hts_codes.csv           # Textile HTS Database
├── src/
│   ├── auditor.py              # Visual Audit Logic
│   ├── agent.py                # Tool-use & Function Calling
│   └── passport_gen.py         # QR & JSON Generation
├── exports/
│   ├── final_dpp_record.json   # Machine-readable passport
│   └── DPP_QR_Code.png         # Physical scan link
└── README.md
🏗️ How it Works (The Pipeline)
Ingestion: The system captures an image of a textile label.

Retrieval: The AI queries the local FAISS index for the specific HTS code (e.g., 6109.10 for Cotton T-shirts).

Verification: The Agent compares the "Label Claim" vs. the "Legal Requirement."

Tool Call: If shipping or tax data is missing, the Agent triggers verify_tax_code() to confirm Pakistan's GSP+ status.

Output: A verified Digital Product Passport is generated and encoded into a QR code.

📝 Resilience & Optimization
Exponential Backoff: The system handles 429 RESOURCE_EXHAUSTED errors gracefully, crucial for high-traffic industrial environments using Free Tier APIs.

Edge-Cloud Hybrid: Heavy reasoning is offloaded to Gemini Flash, while sensitive trade data remains local in the FAISS vector store.

Author: M. Junaid Iqbal

Data Scientist & Textile Engineer Karachi, Pakistan
