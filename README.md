🚗 Vehicle Counter using YOLOv8 + SORT

Real-time vehicle detection and counting system using YOLOv8, OpenCV, and SORT tracking algorithm.

This project detects vehicles (cars, trucks, buses, motorbikes) from a video, tracks them with unique IDs, and counts them when they cross a defined line.

📌 Features

🔍 Real-time object detection using YOLOv8

🎯 Vehicle filtering (car, truck, bus, motorbike)

🧠 Object tracking with SORT algorithm

➖ Line-crossing vehicle counting logic

🎥 Works with video input or webcam

🖼 Mask-based region detection support

🛠 Technologies Used

Python

OpenCV

NumPy

cvzone

YOLOv8 (Ultralytics)

SORT (Simple Online Realtime Tracking)

📂 Project Structure
├── car_counter.py
├── mask.png
├── sort.py
├── images/
│   └── cars.mp4
├── weights/
│   └── yolov8n.pt
⚙️ Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/vehicle-counter-yolov8.git
cd vehicle-counter-yolov8
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv
venv\Scripts\activate   # Windows
3️⃣ Install Dependencies
pip install ultralytics opencv-python cvzone numpy
▶️ How It Works

Loads YOLOv8 model (yolov8n.pt)

Applies a mask to focus detection area

Detects vehicles in each frame

Sends detections to SORT tracker

Assigns unique ID to each vehicle

Counts vehicle when it crosses a predefined line

🚀 Run the Project
python car_counter.py

Press Q to exit the video window.

🎯 Counting Logic

Vehicles are counted when their center point crosses the defined line:

limits = [400, 297, 673, 297]

The system ensures:

Each vehicle is counted only once

Tracking ID prevents duplicate counting
