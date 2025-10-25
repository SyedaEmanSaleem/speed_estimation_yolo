
# 🚗 Vehicle Speed Detection using YOLOv8 & OpenCV

This project implements an intelligent **vehicle speed detection system** that uses **YOLOv8 (Ultralytics)** and **OpenCV** to automatically detect, track, and estimate the **real-time speed (in km/h)** of vehicles in a video.
It can be used for **traffic monitoring**, **speed violation detection**, and **road behavior analysis**.

---

## 📸 Features

✅ Detects multiple vehicle types (cars, trucks, buses, motorbikes)
✅ Estimates real-time vehicle speed (km/h) using calibrated pixel distance
✅ Tracks vehicles across frames for continuous speed calculation
✅ Displays speed on each bounding box dynamically
✅ Automatically saves output video with detections
✅ Lightweight and runs efficiently on CPU or GPU

---

## 🧠 Tech Stack

* **YOLOv8 (Ultralytics)** – Object detection
* **OpenCV** – Video processing and tracking
* **cvzone** – Easy bounding box visualization
* **Python 3.x** – Core language
* **Google Colab / Jupyter Notebook** – Execution environment

---

## ⚙️ How It Works

1. Each frame from the video is processed using the **YOLOv8 model**.

2. Detected vehicles are **tracked** using their bounding box coordinates.

3. The **distance** a vehicle travels (in pixels) between frames is calculated.

4. Using a calibration factor (`METERS_PER_PIXEL`) and frame rate (`FPS`), the **speed (km/h)** is estimated:

   [
   \text{Speed (km/h)} = \frac{\text{Pixel Distance} \times \text{Meters Per Pixel}}{\text{Time (s)}} \times 3.6
   ]

5. The detected speed is displayed on each bounding box and saved in the output video.

---


## 🚀 Setup & Run

### 1️⃣ Install Dependencies

```bash
pip install ultralytics opencv-python cvzone numpy
```

### 2️⃣ Run the Script

```bash
python vehicle_speed_detection.py
```

### 3️⃣ Input/Output Paths

* Input video: `/content/drive/MyDrive/video.mp4`
* Output saved to: `/content/drive/MyDrive/output_vehicle_speed.mp4`

---

## 🧩 Example Output

Each detected vehicle shows its **speed in km/h** above the bounding box.
Green = Normal speed
Red = Overspeed

*(You can include a demo GIF or image here.)*

---

## ⚖️ Calibration Tip

Adjust the value of `METERS_PER_PIXEL` based on your camera angle and video scale for more accurate results.

Example:

```python
METERS_PER_PIXEL = 0.05  # 1 pixel = 0.05 meters
```

---

## 📊 Applications

* Traffic flow monitoring
* Smart city surveillance
* Speed limit enforcement
* Road safety analytics

---

## 🧑‍💻 Author

**Eman**
📧 syedaemansaleem1@gmail.com
🔗 https://github.com/SyedaEmanSaleem

---

## 🏁 License

This project is released under the **MIT License** – feel free to use and modify for your own applications.

---
