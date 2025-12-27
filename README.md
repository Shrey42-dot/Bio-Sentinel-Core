# Bio-Sentinel: Agentic Deepfake Defense System 🛡️

![Status](https://img.shields.io/badge/Status-Prototype-orange) ![Python](https://img.shields.io/badge/Python-3.9+-blue) ![AI](https://img.shields.io/badge/Focus-Computer_Vision-green) ![License](https://img.shields.io/badge/License-MIT-lightgrey)

**Bio-Sentinel** is an Agentic AI cybersecurity solution designed to detect sophisticated deepfakes and "Virtual Injection" attacks in real-time. Unlike traditional passive detectors, Bio-Sentinel employs an active "Challenge-Response" agent and biological signal analysis (rPPG) to verify liveness.

---

## 🚩 The Problem
Current media forensics tools are failing against:
* **GenAI Agents:** Hyper-realistic deepfakes (Sora/Kling) that bypass pixel-level detection.
* **Virtual Camera Injection:** Attackers feeding pre-recorded fake streams directly into KYC/Auth systems, bypassing physical hardware.
* **Passive Failure:** Static liveness checks (blinking/smiling) are easily automated by scripts.

## 🚀 Our Solution: The "Bio-Sentinel" Engine
We propose a multi-modal verification stack that validates the **human**, not just the image.

### Key Features
* **🫀 rPPG Bio-Liveness:** Extracts remote photoplethysmography (heartbeat) signals from facial skin pixels. Generative AI creates perfect pixels, but it cannot simulate a consistent blood flow pulse.
* **🤖 Agentic Challenge-Response:** An autonomous AI agent flashes random color sequences or prompts micro-gestures to measure reaction latency, defeating scripted replay attacks.
* **🔒 Hardware Integrity Layer:** Low-level driver analysis to detect and block "Virtual Camera" software (e.g., OBS, DeepFaceLive) attempting to inject video feeds.
* **⚡ Edge-Optimized:** Uses quantized models (INT8) to run locally on consumer hardware with <50ms latency.

---

## 🏗️ System Architecture

Our ML Pipeline follows a fusion-based approach:

1.  **Input Layer:** Live Video Stream (WebRTC) + Audio Feed.
2.  **ROI Extraction:** **MTCNN** detects and aligns the face mesh.
3.  **Spatial Analysis:** **EfficientNet-B0** scans for pixel-level artifacts and texture inconsistencies.
4.  **Temporal Analysis:** **LSTM/GRU** networks analyze frame sequences for unnatural movement dynamics.
5.  **Bio-Signal Extraction:** **SciPy/OpenCV** extracts rPPG waveforms to verify pulse presence.
6.  **Decision Output:** A weighted fusion layer generates a "Trust Score" (0-100%).

*(See `docs/architecture_diagram.png` for visual workflow)*

---

## 🛠️ Technology Stack

| Component | Technology |
| :--- | :--- |
| **Core AI Framework** | PyTorch / TensorFlow |
| **Computer Vision** | OpenCV, MediaPipe (Face Mesh) |
| **Signal Processing** | SciPy (rPPG extraction) |
| **Backend API** | FastAPI (Python) |
| **Frontend Dashboard** | React.js / Streamlit |
| **Deployment** | Docker Containers |
| **Database** | PostgreSQL (Audit Logs) |

---

## 📦 Installation & Setup (Prototype)

```bash
# Clone the repository
git clone [https://github.com/YourUsername/Bio-Sentinel-Core.git](https://github.com/YourUsername/Bio-Sentinel-Core.git)

# Navigate to directory
cd Bio-Sentinel-Core

# Install dependencies
pip install -r requirements.txt

# Run the local inference server
python main.py --mode=edge
```
## 🛤️ Roadmap
[x] Phase 1: Concept & Architecture Design (Complete)

[ ] Phase 2: rPPG Model Training on SiW Dataset

[ ] Phase 3: Hardware Driver Analysis Module

[ ] Phase 4: Integration with Zoom/Teams API

## 👥 Team
Project Lead: Shrey Pandey 
Hackathon: eRaksha 2026 
Theme: Agentic AI / Deepfake Detection
