# PPE Detection System — Learning Journey

A hands-on learning project building towards a PPE (Personal Protective Equipment) detection system using OpenCV and YOLO.

## What This Is

This repo documents my learning path — from basic image operations all the way to real-time object detection and tracking. Everything is coded step-by-step in a single Jupyter notebook.

## Topics Covered

### 1. OpenCV Basics
- Reading and displaying images
- Webcam capture (live video feed)
- Drawing shapes — rectangles, circles, lines
- Adding text overlay on images

### 2. Image Processing
- Resize and crop
- Grayscale conversion
- Gaussian blur
- Thresholding (binary)
- Edge detection (Canny)

### 3. Region of Interest (ROI)
- Extracting face, hand, and phone regions from images
- Drawing bounding boxes around ROI
- Applying blur to specific regions (face blurring)
- Live ROI extraction from webcam

### 4. Reading & Writing Images
- Saving processed images (`cv2.imwrite`)
- Saving cropped regions (face extraction)
- Saving grayscale versions

### 5. Mini Project — Webcam Tool
- Live webcam with FPS counter
- Bounding box overlay
- Screenshot capture on keypress (`S` to save)
- Graceful exit handling (ESC / window close)

### 6. YOLO Object Detection
- First detection on a static image using YOLOv11 (`yolo11n.pt`)
- Real-time webcam detection with YOLO
- Filtering detections by class (persons only)
- Custom bounding boxes with employee ID labels

### 7. Object Tracking
- Real-time person tracking using YOLOv11m + ByteTrack
- Persistent ID assignment across frames

## Project Structure

```
PPE Detection System/
├── README.md
├── requirements.txt
└── PPE_DETECTION_SYSTEM/
    ├── learning_notebook.ipynb   # All code lives here
    ├── office.png                # Sample test image
    ├── man.jpg                   # Sample test image
    ├── yolo11n.pt                # YOLO nano model
    ├── yolo11m.pt                # YOLO medium model
    ├── result.jpg                # Detection output
    ├── result2.jpg               # Detection output
    ├── face.png                  # Extracted face ROI
    ├── face1.png                 # Extracted face ROI
    ├── gray_image.png            # Grayscale output
    ├── office_copy.png           # Saved copy
    └── screenshot_*.jpg          # Webcam screenshots
```

## Setup

```bash
pip install -r requirements.txt
```

### Requirements
- Python 3.8+
- `ultralytics` — YOLOv11 object detection
- `opencv-python` — Computer vision & image processing

## How to Use

1. Clone the repo
2. Install dependencies: `pip install -r requirements.txt`
3. Open `PPE_DETECTION_SYSTEM/learning_notebook.ipynb` in Jupyter
4. Run cells top to bottom — each cell is a self-contained example

## Status

🟡 **In Progress** — Currently learning the fundamentals. PPE-specific detection (helmets, vests, gloves, etc.) is the end goal.
