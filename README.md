# Human-Detection-and-Pose-Estimation-and-tracking-and-Face-Detection
This project utilizes innovative computer vision technologies, specifically MediaPipe and YOLOv8 (You Only Look Once Version 8), to perform human pose estimation and face detection. The program processes video input extracts human figures using YOLOv8, and then applies pose estimation and face detection on these figures.



1. Libraries and Dependencies 📚
MediaPipe: An open-source library by Google for building pipelines for processing perceptual data, including images and videos.
ultralytics YOLOv8: A real-time object detection system that applies deep neural networks for object detection.
OpenCV (Open-Source Computer Vision Library): Used for video and image processing.
PyTorch: An open-source machine learning library. It's used here to check for CUDA (GPU acceleration) availability and compatibility.
Numpy: A fundamental package for scientific computing with Python.
Datetime: For generating timestamp-based filenames.
Collections: Specifically, the defaultdict is used for efficient data handling.


2. Core Components 🧩
MediaPipe Pose Detector:
Custom poseDetector class: Utilizes MediaPipe's pose solution to detect human poses in the input frames.
Configurable parameters include detection confidence, tracking confidence, and landmark thickness for drawing.

MediaPipe Face Detector:
Custom FaceDetector class: Implements MediaPipe's face detection.
The face detection confidence level is adjustable.
Draws bounding boxes and confidence scores around detected faces.

YOLOv8 Object Detection:
Initialized using a pre-trained model for detecting humans in the video frames.
Extracts bounding boxes of detected human figures.


3. Features and Functionalities 🌈
Pose Estimation on Humans Detected by YOLOv8: For each human detected by YOLOv8, the program performs pose estimation within the bounding box.
Face Detection:
Inside YOLOv8 bounding boxes (localized): Performs face detection on the area inside each detected human figure.
Global face detection: Optionally, face detection can be performed on the entire frame.

Customizable Drawing Options:
Bounding boxes for human detection and face detection.
Pose landmarks and connections.

A line from the nose landmark to the bottom-left corner of the frame.

Human Tracking: Tracks the movement of detected humans across frames.

Real-Time Display Option: The processed frames can be displayed in real-time or processed in the background.
