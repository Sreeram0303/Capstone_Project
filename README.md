# Capstone_Project
This system detects cotton leaf diseases using deep learning. Pipeline 1 uses EfficientNetV2, U-Net, and LIME for accurate classification, precise segmentation, and explainability. Pipeline 2 uses YOLOv11 and SAM for real-time detection and segmentation. Both provide disease type and infection severity.
🌿 Cotton Leaf Disease Detection and Severity Estimation System
✅ Project Objective:
To develop an automated deep learning-based system that can:

Accurately classify cotton leaf diseases.

Precisely segment the infected regions.

Quantify the severity of infection.

Provide explainable outputs to aid in decision-making for farmers and agricultural experts.

🔁 Pipeline 1: EfficientNetV2 + U-Net + LIME
Workflow:

Input Image: Cotton leaf image (healthy or diseased).

EfficientNetV2: Classifies the disease type (e.g., Healthy, Bacterial Blight, Leaf Curl Virus).

HSV Thresholding: Generates a rough mask based on color thresholds.

U-Net Segmentation: Refines disease region segmentation.

Infection Calculation: Computes the percentage of leaf area affected.

LIME Explainability: Visualizes which parts of the image influenced classification.

Final Output: Disease type + Infection severity + Heatmap for explainability.

Key Strengths:

High classification accuracy (up to 98.06%).

Pixel-level segmentation with Dice Score of 0.9834.

Transparent decision-making using LIME.

🔁 Pipeline 2: YOLOv8 + SAM
Workflow:

Input Image: Cotton leaf image from a real-world source.

YOLOv8: Detects and classifies diseased leaves with bounding boxes.

SAM (Segment Anything Model): Segments the infected area with zero-shot capability.

Infection Calculation: Measures the percentage of infection using pixel ratio.

Final Output: Disease type + Severity Level (Mild/Moderate/Severe).

Key Strengths:

Real-time processing with YOLOv8.

High generalization through SAM without retraining.

Minimal manual annotation needed.

