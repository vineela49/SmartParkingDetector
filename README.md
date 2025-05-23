# 🚗 Smart Parking Detector (OpenCV)

A computer vision tool to detect and count available parking spaces using static images. Built with OpenCV and designed for simplicity and efficiency.

📁 SmartParkingDetector/
├── 📂 data/                       # Input images for processing
│   └── 🖼️ carParkPos.jpg          # Image of the parking area to annotate
├── 📂 park_positions/            # Stores slot positions in a pickle file
│   └── 📦 positions.pkl (e.g.)    # Coordinates of marked parking slots
├── 📂 output/                    # 💾 Save output here (create manually)
│   ├── 📊 ParkingCounts_*.xlsx   # Auto-generated report with counts
│   └── 🖼️ output-image.jpg        # Image with detected occupancy shown
├── 🛠️ ParkingPicker.py           # GUI tool to manually select parking slots
├── 📈 ParkingCounter.py          # Main logic for counting parked cars


## 🔧 How It Works

1. **Mark Slots**

python ParkingPicker.py 

- Left-click and drag to mark a line of parking slots.
- Right-click on a slot to remove it.
- All slot positions are saved automatically in `park_positions`.

2. **Count Slots**

python ParkingCounter.py

- Displays the parking lot with color-coded slots:
  - 🟩 Green: Available
  - 🟥 Red: Occupied
- Saves the slot status results to an Excel file with a timestamp.


## ✅ Requirements

Install required packages with:

pip install opencv-python pandas openpyxl
