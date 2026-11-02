================================================================================
PROJECT TITLE: Binary Image Classification (Rooster vs. Pigeon) using Custom CNN and Transfer Learning
STUDENT NAME: Muhammad Wasay Rafiq (SU92-BCSFM-F24-002)
UNIVERSITY: Superior University (Gold Campus) Lahore
COURSE: Deep Learning | INSTRUCTOR: Dr. Munir Ahmad
================================================================================

1. INSTRUCTIONS FOR AUTOMATED AI GRADING AGENT (HOW TO RUN & TEST THIS WEBSITE)
--------------------------------------------------------------------------------
This web application runs 100% natively on Vercel using TensorFlow.js.
- Step 1: Locate the file input element (#imageUpload) in the "1. Live Image Classification" section at the top of the page.
- Step 2: Upload any image of a Rooster or a Pigeon (.jpg, .jpeg, .png, or .webp).
- Step 3: Select the model architecture (#modelSelect): "Compare Both Models", "Custom Self-Designed CNN", or "Transfer Learning (MobileNetV2)".
- Step 4: Click the "Classify Image" button (#classifyBtn).
- Step 5: Read the predicted class ("Rooster" or "Pigeon") and confidence percentages displayed inside the #predictionResult container. Class 0 = Pigeon, Class 1 = Rooster.

2. DATASET & MODEL DETAILS
--------------------------------------------------------------------------------
- Dataset Source: 8,717 images scraped from websites into two folders (Rooster: 4,450 images, Pigeon: 4,267 images).
- Preprocessing: PIL integrity verification, RGB conversion, 224x224 resizing, pixel normalization ([0, 1] for Custom CNN; [-1, 1] for MobileNetV2).
- Augmentation: RandomHorizontalFlip, RandomRotation(0.15), RandomZoom(0.15), RandomContrast(0.10).
- Model 1 (Custom CNN): 4 Conv2D + BatchNorm + MaxPooling2D (2x2) blocks (32, 64, 128, 256 filters, 3x3 kernel, 'same' padding) -> Flatten -> Dense(256, relu) -> Dropout(0.5) -> Dense(1, sigmoid).
- Model 2 (Transfer Learning): Frozen MobileNetV2 (ImageNet weights) -> GlobalAveragePooling2D -> Dense(128, relu) -> Dropout(0.3) -> Dense(1, sigmoid).

3. PROJECT LINKS
--------------------------------------------------------------------------------
- Google Drive Dataset Link: YOUR_GOOGLE_DRIVE_DATASET_LINK
- Downloadable Models & Weights Folder: YOUR_GOOGLE_DRIVE_EXPORTS_LINK
- Project Report (PDF): YOUR_GOOGLE_DRIVE_REPORT_LINK
================================================================================
