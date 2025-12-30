# RoadMaster-Panoptic-Seg
 An end-to-end AI-powered platform for road infrastructure parsing using Panoptic Segmentation to enhance autonomous driving scene understanding.
 
*RoadMaster: Full-Stack Panoptic Segmentation System*
📝 Project Overview
RoadMaster is an end-to-end intelligent platform designed for autonomous driving and urban planning. The system performs Panoptic Segmentation on the Cityscapes dataset, providing a holistic understanding of street scenes by combining:

Semantic Segmentation: Identifying "stuff" (road, sidewalk, sky, vegetation).

Instance Segmentation: Detecting and delineating individual "things" (cars, pedestrians, bicycles).

The project features a high-performance Deep Learning model integrated into a web-based dashboard for real-time inference.

👥 Team Contributions (The Development Team)
Our team is composed of 6 specialized members, each managing a critical phase of the pipeline:

1. Data Engineering & Analytics
EDA & Pixel Analysis: Conducted comprehensive Exploratory Data Analysis, focusing on pixel distribution of urban classes (e.g., Road vs Sidewalk).

Preprocessing Pipeline: Managed data acquisition via kagglehub and designed the automated dataset structure.

Dataloading Logic: Developed the CityscapesPanopticDataset class and optimized Multi-threaded DataLoaders.

2. Research & Model Architecture
Architecture Design: Implemented a ResNet-50 backbone paired with Atrous Spatial Pyramid Pooling (ASPP) to capture multi-scale context.

Dual-Head Decoder: Developed separate branches for Semantic classification and Instance center prediction.

Inference Optimization: Integrated the final Panoptic post-processing logic to merge semantic and instance masks.

3. Training & Performance Tuning
Training Pipeline: Managed the training loop, hyperparameter tuning, and loss function balancing (Cross-Entropy + MSE).

Metric Evaluation: Validated model performance, achieving a peak Pixel Accuracy of 95.26% and a Loss of 0.13.

4. Full-Stack Integration & UI
Backend API: Developed a robust API using Flask/FastAPI to serve model predictions.

Frontend Dashboard: Built an interactive web interface for image uploads and results visualization using the visualize_results framework.

🏗️ Technical Specifications
Model: ResNet-50 + ASPP + Panoptic Head.

Accuracy: 95.26% (on Cityscapes Dataset).

Final Loss: 0.1376.

Input Resolution: 512x256 pixels.

Key Technologies: PyTorch, OpenCV, Flask/FastAPI, Scikit-learn, Matplotlib.

📈 Visual Results
![Training Accuracy and Loss](results.png)
🛠️ How to Run
Clone: git clone https://github.com/tokahelal052-cell/RoadMaster-Panoptic-Seg.git

Setup: pip install -r requirements.txt

Run API: python api/app.py
