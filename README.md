# Simple YOLO Object Detection

A Python program that detects objects in images or from a live webcam using the YOLOv8 Nano model.

## Features

- Detects objects in an image.
- Displays live object detection from a webcam.
- Prints each detected object's name, confidence score, and bounding box coordinates.
- Saves an annotated copy of an image as `output.jpg`.

## Requirements

- Python 3.8 or newer
- A webcam for live detection

## Setup

### 1. Create a virtual environment

**Windows PowerShell:**

```powershell
python -m venv env
.\env\Scripts\Activate.ps1
```

**macOS or Linux:**

```bash
python3 -m venv env
source env/bin/activate
```

### 2. Install dependencies

```bash
pip install ultralytics opencv-python
```

The YOLOv8 Nano weights file (`yolov8n.pt`) downloads automatically the first time you run the program.

## Usage

### Detect objects in an image

```bash
python detect.py image path/to/photo.jpg
```

Replace `path/to/photo.jpg` with the path to your image. The program prints the detections and saves the annotated image as `output.jpg` in the current working directory.

### Detect objects using a webcam

```bash
python detect.py webcam
```

A window opens with the live webcam feed and detection labels. Press **Q** to quit.

## Configuration

The confidence threshold is set to `0.4` in `detect.py`. Detections below this confidence level are ignored.

## Project files

```text
.
├── detect.py
├── README.md
└── .gitignore
```

The `env/` virtual environment folder should be listed in `.gitignore`, so it is not uploaded to Git. The `yolov8n.pt` model weights are downloaded automatically when needed and usually do not need to be uploaded.