# YOLO-defect-detection
This repository contains an end-to-end deep learning system for real-time textile defect detection, focused on identifying hole defects in fabric images. The project uses multiple YOLO architectures (YOLOv8, YOLOv9, YOLOv11, YOLOv12) for benchmarking and selects YOLOv12 as the best-performing model. The final model is converted into TensorFlow Lite and deployed in an offline Android mobile application for real-world inspection.

# Project Highlights
One-class hole defect detection
Trained and compared YOLOv8, YOLOv9, YOLOv11, YOLOv12
Best model: YOLOv12
Performance:
Precision: 85.7%
Recall: 85.8%
mAP@0.5: 87.9%
mAP@0.5–0.95: 37.7%
Converted to TFLite
Deployed as a fully offline Android app
Real-time inference on mobile devices

# Problem Statement
Manual inspection of textile fabrics is slow, costly, and prone to human error. Small defects like holes are often missed, leading to material waste and quality issues. This project aims to automate fabric inspection using deep learning-based object detection that works in real-world conditions and can run on mobile devices.

# System Pipeline
Image Dataset
      ↓
Manual Annotation (Roboflow)
      ↓
Preprocessing & Augmentation
      ↓
YOLOv8 / YOLOv9 / YOLOv11 / YOLOv12 Training
      ↓
Model Evaluation & Comparison
      ↓
Best Model (YOLOv12)
      ↓
ONNX → TensorFlow → TFLite Conversion
      ↓
Android App (Offline Real-Time Detection)

# Mobile Deployment
The trained YOLOv12 model was converted to TensorFlow Lite and integrated into an Android application using Android Studio. The app:
Works completely offline
Uses the device camera for real-time detection
Displays bounding boxes around detected hole defects
Is optimized using quantization for fast mobile inference
