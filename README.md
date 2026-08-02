# IsoFlow Systems - Ephemeral UI Portal

This repository contains the source code for the frontend user interface of **IsoFlow Systems** (deployed at `isoflowai.in`). Built as a highly performant, security-first web application, this UI layer coordinates user document uploads, framework selection, and real-time mapping status streams while maintaining a strict zero-persistence architecture.

---

## 🔒 Security & State Management Architecture

To meet strict enterprise compliance standards, the UI layer operates under a zero-retention data lifecycle:
* **In-Memory Buffering:** Uploaded policy documents (`.pdf`, `.docx`, `.txt`) and compliance matrices (`.csv`) are held strictly within ephemeral session memory.
* **Direct Transit:** Data is transmitted securely via TLS 1.3 to the backend processing logic without passing through or spinning up any persistent local storage or intermediary databases.
* **Instant Session Purge:** The exact moment a user completes their Excel export, closes the browser tab, or terminates the session, all localized states, variable memories, and file streams are completely wiped from RAM.

---

## 🛠️ Tech Stack & Key Features

* **Framework:** Streamlit / Python-based UI ecosystem engineered for rapid execution and low-latency interaction.
* **File Processing Component:** Highly responsive drag-and-drop file ingestion module configured to handle files up to 200MB.
* **Dynamic Feedback Interface:** Real-time state indicators and parsing progress tickers that keep users updated during deep LLM cross-referencing.
* **Design Styling:** Embedded CSS overrides to provide a clean, uncluttered, professional B2B SaaS interface.
