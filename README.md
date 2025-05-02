Video Object Segmentation and Motion Tracking
This project investigates two classical computer vision techniques for segmenting and tracking moving objects in video streams. Designed without deep learning, the solutions are lightweight, interpretable, and well-suited for real-time deployment in constrained environments.

Project Overview
The system supports two distinct approaches:

1. Edge Detection + ORB Feature Tracking
This pipeline uses Canny edge detection to identify object boundaries and tracks keypoints using the ORB (Oriented FAST and Rotated BRIEF) algorithm. It incorporates optical flow, Kalman filtering, and homography transformation for robust tracking.

2. Frame Differencing + Thresholding
This method segments motion by calculating frame-to-frame pixel differences, applying binary thresholding and morphological operations to isolate regions of movement.

Both methods are implemented in Python and presented through a web interface built with Streamlit, allowing users to upload and process videos interactively.

Key Objectives
Detect and segment motion in video sequences using traditional CV methods.

Compare two complementary approaches for motion tracking.

Generate annotated video outputs with overlays for visual interpretation.

Provide an interactive, user-friendly web interface.

Evaluate the performance and use-case suitability of each method.

Implementation Details
Tools and Libraries

Python

OpenCV

NumPy

Streamlit

Google Colab (for prototyping)

Core Steps (both approaches)

Load and preprocess video frames

Apply respective motion segmentation technique

Annotate and compile output video

Visualize results via Streamlit interface

Approach Comparison
Aspect	Approach 1: ORB Tracking	Approach 2: Frame Differencing
Speed	Moderate	Fast
Accuracy	High (keypoint-based)	Lower (sensitive to noise)
Robustness	Invariant to rotation	Better for simple motion

Results
Both methods successfully segment motion across a variety of video types.

ORB-based tracking offers greater accuracy and resilience to noise.

Frame differencing is faster and performs well in scenarios with clear foreground movement.

Deployment
The application is deployed via Streamlit for ease of access and usability. Users can upload their own videos and observe live segmentation and tracking results.

Live App
Streamlit Web App

Colab Notebook (Approach 1)
Google Colab

Demo Video
Watch Demo

Repository Structure
video-segmentation-and-tracking/
│
├── app.py                  # Streamlit app logic
├── edge_orb_tracker.py     # ORB + Edge-based tracking
├── frame_diff_tracker.py   # Frame differencing approach
├── utils.py                # Helper functions
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation

Conclusion
Classical computer vision techniques can still offer effective solutions for video segmentation and object tracking, especially in scenarios where deep learning is impractical. This project demonstrates the viability of such methods in real-time applications, offering trade-offs between performance, speed, and complexity.
