# Multi-Agent AI System for Wildlife Detection Using YOLOv8

**University of Newcastle · Business Analytics · 2024**  
`Python` `YOLOv8` `Computer Vision` `Object Detection` `Multi-Agent AI` `Deep Learning` `Jupyter Notebook`

---

## 📌 Project Overview

Wildlife monitoring and conservation efforts rely increasingly on automated detection technology to track animal populations, detect poaching activity, and monitor biodiversity at scale. Manual image review is time-consuming and impractical across large geographic areas and continuous camera trap footage. This project implements a **multi-agent AI system using YOLOv8 object detection** to automatically identify and classify wildlife in images and video — demonstrating applied deep learning for a real-world environmental and operational use case.

---

## 🎯 Business / Operational Problem

Conservation organisations, national parks, and wildlife management agencies face a common data challenge:
- Camera traps and drones generate thousands of images per day that cannot be manually reviewed at scale
- Delayed detection of rare species or poaching activity reduces the effectiveness of conservation responses
- Manual classification is expensive, slow, and subject to human fatigue and inconsistency

An automated, AI-powered detection system addresses these challenges by providing **real-time, scalable, consistent wildlife identification** across large image and video datasets.

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `*.ipynb` | Jupyter Notebook — full pipeline: model setup, image preprocessing, YOLOv8 inference, multi-agent coordination, results visualisation |
| `*.py` | Agent scripts for detection, classification, and result aggregation |
| Dataset | Wildlife image dataset used for detection and model evaluation |
| `*.pdf` | Project report — system design, methodology, results, and business application |

---

## 🔧 System Design & Methodology

### Architecture: Multi-Agent Approach

Rather than a single monolithic model, this project uses a **multi-agent design** where specialised agents handle distinct tasks in the detection pipeline:

| Agent | Role |
|---|---|
| **Detection Agent** | Runs YOLOv8 inference to locate and classify wildlife objects in each image frame |
| **Tracking Agent** | Monitors detected objects across frames to track individual animals |
| **Reporting Agent** | Aggregates detection results, generates summary statistics, and flags high-confidence sightings |

This modular design mirrors real-world AI system architecture — agents can be updated or replaced independently, improving system maintainability and scalability.

### 1. Model: YOLOv8
- **You Only Look Once (YOLO)** is a state-of-the-art real-time object detection framework
- YOLOv8 processes the entire image in a single forward pass, enabling fast inference suitable for video streams
- Pre-trained on large-scale image datasets; fine-tuned or applied directly to wildlife imagery in this project

### 2. Image Preprocessing
- Loaded and resized wildlife images to YOLOv8 input specifications
- Applied normalisation and augmentation to improve detection robustness across lighting and environmental conditions

### 3. Detection & Classification
- Ran YOLOv8 inference across the dataset to detect and classify wildlife species in each image
- Generated bounding boxes, class labels, and confidence scores for each detected object
- Filtered detections by confidence threshold to reduce false positives

### 4. Results Aggregation & Visualisation
- Compiled detection results across all images into a structured summary
- Visualised bounding boxes and labels overlaid on source images
- Produced summary statistics: species frequency, confidence distributions, detection rates

---

## 📊 Key Results

| Metric | Description |
|---|---|
| Detection Accuracy | YOLOv8 achieved high precision in identifying wildlife in clear-visibility images |
| Inference Speed | Real-time capable — suitable for live camera feed processing |
| Multi-Agent Coordination | Agents successfully divided detection, tracking, and reporting tasks without conflict |
| Species Classification | Correctly classified multiple wildlife species from the dataset |

> **Outcome:** The multi-agent YOLOv8 system demonstrated the viability of automated wildlife detection for conservation operations — significantly reducing the manual image review burden and enabling faster identification of rare or concerning animal behaviour.

---

## 💡 Business & Operational Value

| Application | Value Delivered |
|---|---|
| Conservation monitoring | Automated population tracking without manual review |
| Anti-poaching operations | Real-time alerts when target species are detected in restricted zones |
| Research & biodiversity studies | Fast, consistent species classification across large image datasets |
| Park management | Operational dashboards showing wildlife movement and hotspot mapping |

---

## 🛠️ Tools & Libraries

| Category | Tools |
|---|---|
| Language | Python 3 |
| Object Detection | YOLOv8 (Ultralytics) |
| Deep Learning | PyTorch |
| Data Processing | Pandas, NumPy, OpenCV |
| Visualisation | Matplotlib, OpenCV drawing tools |
| Environment | Jupyter Notebook |

---

## ⚠️ Limitations & Considerations

- Model performance degrades in low-light, occluded, or heavily obscured images — common in real field conditions
- Fine-tuning on a domain-specific wildlife dataset would improve classification accuracy beyond the base YOLOv8 model
- Multi-agent coordination adds system complexity — production deployment would require robust error handling and agent monitoring
- Ethical use: AI wildlife detection systems must be deployed with appropriate data governance, privacy safeguards, and Indigenous land rights considerations where applicable

---

*Project completed as part of the Bachelor of Business Analytics at the University of Newcastle, 2024.*
