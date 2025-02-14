# Real-Time Object Detection with OpenCV and Python

This project implements a real-time object detection system using OpenCV and the MobileNet SSD (Single Shot Detection) model. The system can detect multiple objects from your webcam feed with good accuracy while maintaining real-time performance.

## Features

- Real-time object detection using webcam
- Multiple object detection in a single frame
- Display of object class names and confidence scores
- High-performance detection using MobileNet SSD model
- Support for COCO dataset classes

## Prerequisites

Before running this project, make sure you have the following installed:
- Python 3.x
- OpenCV (`opencv-python`)
- NumPy

You can install the required packages using pip:
```bash
pip install opencv-python numpy
```

## Required Files

The project requires the following files to run:
- `main.py` - The main Python script
- `coco.names` - File containing the COCO dataset class names
- `ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt` - Model configuration file
- `frozen_inference_graph.pb` - Pre-trained model weights

## How It Works

1. The program initializes the webcam and sets up the video capture parameters
2. Loads the COCO class names from `coco.names`
3. Initializes the MobileNet SSD model with the configuration and weights
4. For each frame from the webcam:
   - Performs object detection using the model
   - Draws bounding boxes around detected objects
   - Displays class names and confidence scores
   - Shows the processed frame in real-time

## Code Overview

The main components of the code include:

- Video capture setup with custom resolution (1280x720)
- Model configuration with specific input parameters
- Detection loop that processes each frame
- Visualization of results with bounding boxes and text

## Usage

1. Clone this repository
2. Ensure all required files are in the same directory
3. Run the script:
```bash
python main.py
```

## Configuration

You can adjust several parameters in the code:
- `thres`: Detection confidence threshold (default: 0.45)
- Video capture parameters:
  - Resolution: 1280x720
  - Brightness: 70
- Model input size: 320x320

## Output

The program will open a window showing the webcam feed with:
- Green bounding boxes around detected objects
- Class names in uppercase
- Confidence scores as percentages

Press 'Q' to quit the application.

## Model Details

This project uses the MobileNet SSD model trained on the COCO dataset, which can detect 80+ different object classes. The model provides a good balance between speed and accuracy, making it suitable for real-time applications.
