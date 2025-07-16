License Plate Detection & Recognition

This repository contains my end-to-end project for detecting and recognizing license plates in vehicle images.  
It was developed to demonstrates my understanding of computer vision, data preprocessing, and deep learning basics.

---------------------------------------------------------------------------------------------------------------------------------------------------------------

Project Overview

Objective: 
Detect license plates in car images (predict bounding box coordinates).  
Recogniz the alphanumeric characters on the detected plates (OCR task).

Datasets:  
- Training Set 1: Full vehicle images + bounding boxes (900 images)  
- Training Set 2: Cropped license plates + text labels (900 images)  
- Test Set: Images similar to Training Set 1 (201 images)

-----------------------------------------------------------------------------------------------------------------------------------------------------------

Key Steps

1. Data Loading & Analysis
- Loaded CSV annotations using `pandas`.
- Checked for missing values.
- Visualized random samples with bounding boxes (`OpenCV`, `matplotlib`).
- Analyzed bounding box size distributions, text length, and character frequencies.

2. Detection Pipeline
- Built a PyTorch CNN to predict bounding boxes.
- Normalized coordinates to handle varying image sizes.
- Implemented image preprocessing (resize, normalize).

3. Recognition Pipeline
- Preprocessed cropped plates (grayscale, resize, normalize).
- Encoded text labels to numeric format.
- Built a simple PyTorch CNN for per-character prediction.
- Tracked training/validation loss and accuracy.
- Visualized metrics with plots.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Tools & Libraries

Python 3.x
- `pandas`, `OpenCV (cv2)`, `matplotlib`
- `PyTorch` for model development and training

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Current Status

- Detection and recognition models defined and trained on sample batches.
- Detection training loop partially implemented (full IoU-based evaluation pending).
- Recognition model shows good training accuracy on sample runs.
- Integrated pipeline (detect ➜ crop ➜ recognize) outlined for future work.

---------------------------------------------------------------------------------------------------------------------------------------------------------------

How to Run

Clone this repo:  
```bash
git clone https://github.com/Muskan210/License_Plate_Detection.git
