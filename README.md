# 🚨 Vehicle Theft Detection System

![YOLOv8](https://img.shields.io/badge/YOLO-v8-blue) ![Python](https://img.shields.io/badge/Python-3.12-yellow) ![PyTorch](https://img.shields.io/badge/PyTorch-2.9.0-red) ![License](https://img.shields.io/badge/License-MIT-green)

> A high-performance computer vision model designed to detect vehicle theft scenarios in real-time with **98% precision**.

[Insert a Banner Image or a GIF of the model in action here]

## 📖 Overview
This project implements a custom-trained **YOLOv8** object detection model capable of identifying vehicle thieves. Utilizing a dataset from Roboflow, the system is optimized for speed and accuracy, making it suitable for deployment in security surveillance systems and smart parking solutions.

The model achieves an inference speed of **~10.1ms** on a Tesla T4, allowing for real-time processing of video feeds.

## 📂 Dataset
The model was trained on the **Vehicle Thief Detection** dataset hosted on Roboflow.
* **Source:** [Roboflow Universe - CV Projects XTGOE](https://universe.roboflow.com/cv-projects-xtgoe/vehicle-thief-detection)
* **Preprocessing:** Auto-orientation and resizing.

## ⚙️ Tech Stack & Environment
The training and validation were performed in the following environment:

| Component | Specification |
| :--- | :--- |
| **Framework** | Ultralytics YOLOv8.3.232 |
| **Language** | Python 3.12.12 |
| **Core Library** | Torch 2.9.0+cu126 |
| **Hardware Acceleration** | NVIDIA CUDA:0 (Tesla T4, 15GB VRAM) |

## 📊 Performance Metrics
The model exhibits exceptional performance on the test set (21 images).

### Key Results
| Metric | Value | Description |
| :--- | :--- | :--- |
| **mAP@50** | **0.980** | Mean Average Precision at 0.5 IoU threshold. |
| **Precision** | **0.945** | Ability to identify only relevant objects. |
| **Recall** | **0.952** | Ability to find all relevant objects. |
| **mAP@50-95** | **0.567** | Average over multiple IoU thresholds (robustness). |

### Inference Speed
* **Pre-process:** 4.4ms
* **Inference:** 10.1ms
* **Post-process:** 1.4ms
* **Total per image:** ~15.9ms

## 🖼️ Validation Samples
Below are sample results from the validation batch:

![Sample Detection](path/to/your/val_batch_pred.jpg)
*(Replace this path with an image from your runs/detect/val3 folder)*

## 🚀 Installation & Usage

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/vehicle-thief-detection.git](https://github.com/your-username/vehicle-thief-detection.git)
cd vehicle-thief-detection
