# AI-Based Worker Safety Compliance Detection

An AI-based Computer Vision system for automated PPE compliance and workplace safety monitoring. The system detects workers, hardhats, safety vests, and safety violations from workplace images using YOLO-based object detection models.

## Project Overview

Manual PPE monitoring can be time-consuming and difficult to perform consistently in busy industrial and construction environments. This project provides an automated approach for detecting PPE compliance and identifying potential safety violations.

## Dataset

- WorkerSafety25 dataset from Roboflow Universe
- 8,316 annotated images
- Object Detection task
- 5 selected classes: Person, Hardhat, No-Hardhat, Safety-Vest, No-Safety-Vest
- Bounding-box annotations

## Model Development

The project included data preprocessing, augmentation, model training, and evaluation.

Three YOLO-based object detection models were trained and compared:

- YOLOv8n
- YOLOv9t
- YOLO26n

Models were evaluated using Precision, Recall, mAP@0.5, mAP@0.5:0.95, confusion matrices, and per-class metrics.

## Results

YOLOv8n achieved the strongest overall performance:

- Precision: 0.870
- Recall: 0.841
- mAP@0.5: 0.860
- mAP@0.5:0.95: 0.620

YOLOv8n was selected as the final model for the worker safety monitoring system.

## System Features

- PPE and worker detection
- Safety violation detection
- Image and video processing
- Safety inspection report generation
- Interactive user interface
- LLM + RAG integration for retrieving relevant safety rules and generating safety recommendations

## Project Workflow

Data Acquisition → Preprocessing & Augmentation → Model Training → Model Evaluation → System Integration → LLM + RAG

## Project Structure

```text
AI-Based-Worker-Safety-Compliance-Detection/
├── notebooks/
│   ├── 01_Data_Preparation.ipynb
│   ├── 02_Data_Augmentation.ipynb
│   ├── 03_Model_Development.ipynb
│   ├── 04_Model_Training.ipynb
│   └── 05_Worker_Safety_Final_App.ipynb
├── results/
├── app/
├── README.md
└── requirements.txt
