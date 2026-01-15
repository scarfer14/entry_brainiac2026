# ESP32-Based Keyword Spotting System for Parkinson’s Disease

This repository contains the source code, documentation, and development structure for an **ESP32-based voice keyword spotting (KWS) system** designed to assist patients with **Parkinson’s disease**. The system focuses on detecting predefined spoken keywords and displaying the recognized word on an LCD screen.

The project follows a **Hybrid Development Methodology**:
- **Waterfall** for hardware design and integration
- **Agile** for machine learning model development and training

---

## Project Overview

Parkinson’s disease often causes motor speech impairments, making verbal communication difficult. This project demonstrates a **lightweight embedded keyword spotting system** capable of recognizing simple spoken words using on-device inference.

### Key Features
- ESP32 (38-pin) development board
- INMP441 digital microphone (I2S interface)
- LCD display for real-time feedback
- On-device keyword spotting (TinyML)
- Portable battery-powered design

> **Disclaimer:**  
> This project is intended for **educational and demonstration purposes only** and is not a medical diagnostic tool.

## System Architecture

```text
Patient Voice
     ↓
INMP441 Microphone
     ↓
ESP32
 ├─ Audio Capture (I2S)
 ├─ Feature Extraction (MFCC)
 ├─ Keyword Spotting Model
 └─ LCD Display Output
```


## Hardware Components

- ESP32 38-pin Development Board
- INMP441 I2S Microphone
- LCD Display (I2C)
- TP4056 LiPo Charging Module
- 2000mAh 3.7V LiPo Battery
- Enclosure Box

---

## Repository Structure

parkinsons-kws-esp32/
│
├── data/                  # Audio datasets (ignored in Git)
│   ├── raw_audio/
│   └── processed/
│
├── training/              # Python scripts for ML training
│   ├── preprocess.py
│   ├── model.py
│   ├── train.py
│   └── export_tflite.py
│
├── model/                 # Trained model files
│   ├── kws_model.tflite
│   └── kws_model.h
│
├── esp32/                 # ESP32 firmware
│   ├── main.ino
│   ├── audio_capture.h
│   ├── feature_extraction.h
│   ├── model.h
│   └── lcd_display.h
│
├── docs/                  # Documentation and diagrams
│   ├── architecture.png
│   └── demo_notes.md
│
├── .gitignore
└── README.md



---

## Getting Started (Beginner Guide)

### Option 1: Fork the Repository (Recommended)

Forking creates your own copy of this repository on GitHub.

1. Open this repository on GitHub
2. Click the **Fork** button (top-right)
3. Choose your GitHub account

Clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/parkinsons-kws-esp32.git
cd parkinsons-kws-esp32
