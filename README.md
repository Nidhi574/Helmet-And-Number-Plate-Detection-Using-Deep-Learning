# 🛵 Helmet and Number Plate Detection Using Deep Learning

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg)
![YOLO](https://img.shields.io/badge/YOLO-Object%20Detection-red.svg)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

# Helmet and Number Plate Detection Using Deep Learning

A deep learning-based intelligent traffic monitoring system that automatically detects **motorcycles**, determines whether the rider is wearing a **helmet**, and extracts the **vehicle number plate** using computer vision techniques.

This project aims to improve **road safety**, assist **traffic law enforcement**, and reduce the need for manual monitoring by automating helmet violation detection. It leverages modern deep learning object detection models to provide accurate, real-time analysis from images, recorded videos, or live CCTV feeds.

---

# 📖 Table of Contents

- Introduction
- Project Overview
- Objectives
- Features
- System Architecture
- Workflow
- Technologies Used
- Deep Learning Models
- Dataset
- Project Structure
- Installation
- Usage
- Detection Pipeline
- Results
- Performance
- Applications
- Advantages
- Limitations
- Future Enhancements
- Screenshots
- Contributing
- License
- Author

---

# 📌 Introduction

Road traffic accidents continue to be a major concern worldwide. One of the most common traffic violations is riding motorcycles without wearing protective helmets. Manual monitoring of such violations through CCTV footage is time-consuming, labor-intensive, and prone to human error.

This project introduces an automated solution capable of:

- Detecting motorcycles
- Identifying riders
- Checking helmet usage
- Detecting vehicle number plates
- Extracting registration numbers for further processing

Using state-of-the-art deep learning models, the system performs object detection with high accuracy and can operate in real-time, making it suitable for deployment in intelligent transportation systems.

---

# 🚀 Project Overview

Helmet and Number Plate Detection Using Deep Learning is a computer vision application designed to monitor motorcycles on roads. The application processes images or video streams, identifies motorcycles and riders, determines whether helmets are present, and localizes vehicle number plates.

Once the number plate is detected, it can optionally be passed through an OCR (Optical Character Recognition) engine such as EasyOCR or Tesseract to extract the registration number.

The complete workflow provides a fully automated pipeline for traffic surveillance.

---

# 🎯 Objectives

The primary objectives of this project are:

- Detect motorcycles accurately
- Identify motorcycle riders
- Detect helmet usage
- Identify riders without helmets
- Detect vehicle number plates
- Extract number plate regions for OCR
- Enable automated traffic law enforcement
- Reduce manual monitoring efforts
- Improve road safety through AI-based surveillance

---

# ⭐ Features

## Motorcycle Detection

Detects motorcycles from images and videos using deep learning.

## Helmet Detection

Classifies whether riders are wearing helmets.

## Number Plate Detection

Locates vehicle registration plates with high precision.

## Real-Time Processing

Supports live webcam or CCTV video streams.

## Multiple Object Detection

Can detect multiple motorcycles simultaneously.

## High Accuracy

Uses advanced object detection algorithms for reliable predictions.

## Image Processing

Supports:

- JPG
- PNG
- JPEG
- BMP

## Video Processing

Supports:

- MP4
- AVI
- MOV
- MKV

## Bounding Box Visualization

Displays colored bounding boxes around detected objects.

---

# 🏗️ System Architecture

```
Input Image / Video
          │
          ▼
Image Preprocessing
          │
          ▼
Object Detection Model
          │
          ▼
─────────────────────────────
│ Motorcycle Detection      │
│ Helmet Detection          │
│ Number Plate Detection    │
─────────────────────────────
          │
          ▼
Detection Results
          │
          ▼
OCR (Optional)
          │
          ▼
Vehicle Number Extraction
          │
          ▼
Final Output
```

---

# 🔄 Workflow

### Step 1

Input an image, video, or live camera feed.

↓

### Step 2

Perform image preprocessing including resizing and normalization.

↓

### Step 3

Run the trained object detection model.

↓

### Step 4

Detect:

- Motorcycle
- Rider
- Helmet
- Number Plate

↓

### Step 5

Classify helmet status.

↓

### Step 6

Extract number plate region.

↓

### Step 7

(Optional) Perform OCR to read the registration number.

↓

### Step 8

Display annotated output.

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| OpenCV | Image Processing |
| NumPy | Numerical Computation |
| YOLO | Object Detection |
| TensorFlow / PyTorch | Deep Learning Framework |
| EasyOCR / Tesseract | Number Plate Recognition |
| Matplotlib | Visualization |
| Pandas | Data Handling |

---

# 🧠 Deep Learning Models

The project utilizes modern object detection networks capable of detecting multiple objects in a single image.

Possible models include:

- YOLOv5
- YOLOv8
- Faster R-CNN
- SSD
- EfficientDet

Among these, YOLO is preferred because of its:

- High speed
- High accuracy
- Real-time inference
- Low latency

---

# 📂 Dataset

The dataset consists of annotated images containing motorcycles with and without helmets.

### Classes

- Motorcycle
- Rider
- Helmet
- No Helmet
- Number Plate

The dataset should contain diverse samples including:

- Daytime images
- Nighttime images
- Rainy weather
- Different camera angles
- Various traffic conditions
- Different motorcycle models

---

# 📁 Project Structure

```
Helmet-And-Number-Plate-Detection-Using-Deep-Learning/
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── models/
│
├── weights/
│
├── images/
│
├── videos/
│
├── outputs/
│
├── notebooks/
│
├── utils/
│
├── main.py
├── detect.py
├── train.py
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Helmet-And-Number-Plate-Detection-Using-Deep-Learning.git
```

Move into the project directory

```bash
cd Helmet-And-Number-Plate-Detection-Using-Deep-Learning
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Usage

### Detect from Image

```bash
python detect.py --image image.jpg
```

### Detect from Video

```bash
python detect.py --video video.mp4
```

### Detect Using Webcam

```bash
python detect.py --camera 0
```

---

# 🔍 Detection Pipeline

The system performs the following operations:

1. Capture image or frame.
2. Resize the image.
3. Normalize pixel values.
4. Pass image through object detection model.
5. Detect motorcycles.
6. Detect riders.
7. Detect helmets.
8. Detect number plates.
9. Draw bounding boxes.
10. Save or display results.
11. Perform OCR if enabled.

---

# 📊 Results

The model successfully detects:

- Motorcycle
- Rider
- Helmet
- Number Plate

The output image includes:

- Bounding boxes
- Class labels
- Confidence scores

Example output:

```
Motorcycle - 98%

Helmet - 96%

Number Plate - 94%
```

---

# 📈 Performance

Typical performance depends on hardware and dataset quality.

| Metric | Value |
|---------|--------|
| Precision | High |
| Recall | High |
| mAP | High |
| FPS | Real-Time (GPU) |

Performance may vary depending on:

- GPU
- Image resolution
- Dataset quality
- Number of objects

---

# 🌍 Applications

This project can be used in:

- Smart Cities
- Intelligent Transportation Systems
- Highway Surveillance
- Traffic Monitoring
- Automated Challan Systems
- Police Surveillance
- Road Safety Enforcement
- Toll Booth Monitoring
- Parking Management
- AI-Based CCTV Analytics

---

# ✅ Advantages

- Fully automated detection
- Real-time processing
- High detection accuracy
- Reduces manual intervention
- Supports multiple vehicles
- Easily scalable
- Cost-effective monitoring
- Improves road safety
- Assists law enforcement agencies

---

# ⚠️ Limitations

- Performance depends on dataset quality.
- Low lighting may reduce accuracy.
- Heavy occlusion can affect detection.
- Motion blur may impact number plate localization.
- OCR accuracy depends on image clarity.
- Extreme weather conditions can reduce performance.

---

# 🚀 Future Enhancements

Potential improvements include:

- Automatic challan generation
- Cloud deployment
- Mobile application integration
- License plate OCR improvements
- Helmet color classification
- Rider identification
- Face recognition integration
- Multi-camera support
- Traffic analytics dashboard
- Vehicle tracking across cameras
- Speed detection
- Violation history database
- Edge AI deployment using NVIDIA Jetson or Raspberry Pi

---

# 📸 Screenshots

Add screenshots of:

- Input Image
- Helmet Detection
- Number Plate Detection
- Final Output
- Live Camera Detection

Example:

```
screenshots/
├── input.png
├── helmet_detection.png
├── number_plate.png
├── output.png
└── realtime_detection.png
```

---

# 🤝 Contributing

Contributions are welcome!

To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Push the branch.
5. Open a Pull Request.

Please ensure your code follows clean coding practices and includes proper documentation.

---

# 📜 License

This project is licensed under the MIT License.

You are free to use, modify, and distribute this project for educational and research purposes.

---

# 👨‍💻 Author

**Kushal S A**

AI & Machine Learning Engineer

### Skills

- Python
- Deep Learning
- Machine Learning
- Computer Vision
- OpenCV
- TensorFlow
- PyTorch
- YOLO
- CNN
- OCR
- Data Analysis

---

## ⭐ Support

If you found this project useful:

- ⭐ Star this repository
- 🍴 Fork it
- 🛠️ Contribute to improvements
- 📢 Share it with others

Your support helps improve and maintain this project.
