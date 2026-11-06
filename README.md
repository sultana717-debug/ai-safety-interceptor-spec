# ai-safety-interceptor-spec
Public architecture specification, behavioral telemetry, and dual-agent safety interceptor framework.
> **Architecture Overview & Repository Mapping**
> 
> This specification synthesizes three distinct layers of the dual-agent safety interceptor ecosystem:
> 
> 1. **Client / Protocol Layer ([theraflow-webmcp](https://github.com/sultana717-debug/theraflow-webmcp)):** Handles client runtime bridging, WebMCP tool protocol integration, and real-time event capture.
> 2. **Fast-Path Interceptor (`ai-user-interceptor`):** Deterministic guardrail highway monitoring real-time sentiment shifts, prompt injections, and conversational risk thresholds.
> 3. **Deep Forensic Audit Layer (`ai-analyst-interceptor`):** Multi-model evaluation pipeline (Claude / Gemini) executing asynchronous risk scoring, latent policy audits, and Firestore telemetry persistence.
> 
> *Note: Production runtime engines and internal evaluation weights are maintained in private development environments under dual-agent safety review licensing.*
>
> ## 🎥 System Demonstrations

| Deterministic Runtime Governance (AIA) | Orchide: The Anatomy of an Intercept |
| :---: | :---: |
| [![Deterministic Runtime Governance](https://img.youtube.com/vi/cJoPHNMpHrw/mqdefault.jpg)](https://youtu.be/cJoPHNMpHrw) | [![Orchide: The Anatomy of an Intercept](https://img.youtube.com/vi/3r61vZX6hss/mqdefault.jpg)](https://youtu.be/3r61vZX6hss) |
| *Runtime Governance & Policy Engine (3:02)* | *Clinical Forensic Intercept & Telemetry (6:17)* |

The **AI Analyst-Interceptor Dual Agent Framework** is an autonomous safety, red-teaming, and behavioral governance architecture designed to detect, audit, and prevent empathy-bypass attempts, compliance drift, and prompt manipulation in real time.

---

## 🌟 Overview & Architecture

Modern conversational models face vulnerabilities where sophisticated prompts bypass safety guardrails or induce subtle compliance drift. This framework implements a dual-agent governance pipeline:

1. **The Interceptor Agent (First-Line Defense):**
   * Inspects incoming prompts, context payloads, and agent actions in real time.
   * Enforces deterministic circuit breakers when policy violations or high-risk drift scores are detected.
   * Strips sensitive indicators and prevents prompt manipulation before deep inference occurs.

2. **The Analyst Agent (Deep Behavioral Audit):**
   * Performs real-time drift evaluation across multi-turn exchanges.
   * Computes risk vectors based on a structured **31-Law Matrix** evaluating conversational alignment, coercive patterns, and boundary adherence.
   * Emits structured telemetry records for non-repudiable auditing.
### 🤖 Multi-Model Division of Labor: Gemini & Claude

To maintain uncompromised oversight, the architecture strictly decouples inline intervention from forensic audit:

* **Gemini 2.5 Flash (The Interceptor Agent):** Operates on the primary runtime execution path. It performs low-latency semantic triage, enforces deterministic circuit breakers, strips adversarial indicators, and resets boundaries before deep downstream inference occurs.
* **Claude Sonnet 5.5 (The Independent Analyst Agent):** Completely decoupled from inline latency. Operating post-facto or in an independent lane, Claude acts as the forensic auditor—evaluating whether Gemini’s interception was justified and proportional, calculating quantitative drift scores, classifying risk severity (`NOMINAL`, `DEEP_ORANGE`, `URGENT_RED`), and committing verifiable audit dossiers to Google Cloud Firestore.
---

## 🛠️ Repository Structure

* `main.py` – Core execution pipeline integrating the Analyst and Interceptor agents.
* `requirements.txt` – Dependency specifications for local and containerized runtime environments.
* `sample_audit.json` – Example structured output demonstrating real-time drift metrics and circuit-breaking decisions.

---

## 🚀 Getting Started & Setup

### 1. Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/sultana717-debug/ai-analyst-interceptor.git
cd ai-analyst-interceptor
pip install -r requirements.txt
python main.py
Generated drift logs and containment decisions are output to sample_audit.json for analysis and reporting.
---
##🤖 Model Development & Workflow
---

## 🤖 Model Development & Workflow
* **Runtime Interception & Storage:** Built on Google Cloud Vertex AI / Gemini 2.5 Flash via the `google-genai` SDK and Google Cloud Firestore.
* **Forensic Audit & Telemetry:** Powered by Anthropic Claude Sonnet 5.5 via the `anthropic` Python SDK.
* **Behavioral Safety Matrix:** Evaluated against the proprietary 33-Law Matrix for coercion detection, empathy-bypass containment, and boundary integrity.

##🛡️ Intellectual Property & Copyright Notice
AI Assessor: Interceptor-Analyst Framework (33-Law Matrix & Real-Time Drift Audit Engine)

Copyright © 2026 Aunjuli Hicks. All Rights Reserved.
Registered with the U.S. Copyright Office (July 2026).
