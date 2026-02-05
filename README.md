Chickpea Anomaly Detection using YOLOv5

An end-to-end deep learning system that classifies chickpeas into 7 quality grades using the YOLOv5 object detection architecture. This project is built to automate and optimize chickpea quality control with real-time field deployment in mind.

![YOLOv5 Detection Sample](./sample_output.png) <!-- Optional: Include a sample image if available -->

 📌 Project Overview

This project leverages YOLOv5 to detect and classify chickpeas from images into 7 quality categories based on visual anomalies. The model was trained on over 20,000 annotated images and integrates OpenCV for preprocessing and PyTorch for model training and inference. The system also includes visualization tools and deployment planning for real-world usage.

---

 🚀 Features

- ✅ Trained YOLOv5 model on 20K+ custom-labeled chickpea images
- ✅ Achieved 96.4% classification accuracy
- ✅ Efficient preprocessing with OpenCV and PyTorch
- ✅ Real-time inference readiness with Flask and Android app integration planned
- ✅ Training metrics tracked using TensorBoard and Matplotlib


---

 📂 Directory Structure
Chickpea-Anomaly/ │ ├── dataset/ # Raw and preprocessed images ├── annotations/ # YOLOv5 format labels ├── models/ # Trained weights (.pt files) ├── src/ │ ├── train.py # Training script │ ├── detect.py # Inference script │ └── utils.py # Helper functions (preprocessing, visualization) ├── app/ │ ├── flask_api.py # Flask API (for future deployment) │ └── android_integration/ # Placeholder for Android app integration ├── runs/ # TensorBoard logs and training outputs ├── requirements.txt └── README.md


---

 🧠 Model Details

- **Model:** YOLOv5 (custom trained)
- **Input Size:** 640x640
- **Classes:** 7 chickpea quality grades
- **Optimizer:** SGD
- **Loss Function:** YOLOv5 default loss (CIoU + objectness + class loss)
- **Training Time:** Reduced by 25% using optimized image processing and data loading

---

 🛠️ Setup Instructions

1. **Clone the Repository**
```bash
git clone https://github.com/utk1725/Chickpea-Anomaly-.git
cd Chickpea-Anomaly-
Create and Activate Virtual Environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install Requirements
pip install -r requirements.txt
Train the Model
python src/train.py --img 640 --batch 16 --epochs 100 --data data.yaml --weights yolov5s.pt
Run Inference
python src/detect.py --weights models/best.pt --img 640 --source dataset/test/
📊 Visualization Tools

TensorBoard:
tensorboard --logdir=runs
Matplotlib: Custom training curves for loss, accuracy, and mAP.
📱 Deployment Plan (Upcoming)

🔧 Flask API for real-time inference
📱 Android integration for in-field classification and feedback
☁️ Cloud storage for annotated images and results
📘 License

This project is licensed under the MIT License.

📄 Project Report

You can download or view the full project report here.

🙌 Acknowledgements

YOLOv5 by Ultralytics
TensorBoard and PyTorch communities
Chickpea sample dataset manually annotated for this project
