# VPlay
Court Line Detection & Tracking Project �📹

This project uses YOLOv8 and YOLOv5 with tracking algorithms to detect and analyze court lines, player movement, and ball tracking in tennis videos.

## 🧠 Project Structure

| File/Folder         | Description |
|---------------------|-------------|
| `main.py`           | Entry point script |
| `trackers/`         | Player and ball tracking modules |
| `court_line_detector/` | Court line detection logic |
| `mini_court/`       | Mini court visualization |
| `utils/`            | Utility functions for video processing |
| `constants/`        | Project constants |
| `training/`         | Training notebooks and data configs |
| `analysis/`         | Analysis notebooks |
| `input_videos/`     | Raw video inputs (not included) |
| `output_videos/`    | Output with detections (generated) |
| `models/`           | Model files (see models/README.md) |

---

## 📥 Model Files Required

This project requires several model files that are not included in the repository due to their size:

1. **yolov8x.pt** - YOLOv8 extra-large model for player detection
   - Download from: [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
   - Place in project root directory

2. **Model files in `models/` directory**:
   - `yolo5_best.pt` - Ball detection model
   - `yolo5_last.pt` - Ball detection model (last checkpoint)
   - `keypoints_model.pth` - Court keypoints model
   - See `models/README.md` for details

---

## ⚙️ Setup

```bash
git clone https://github.com/vivekrajsingh04/court-vision.git
cd court-vision

# Create virtual environment
python -m venv venv
source venv/bin/activate   # on Windows: venv\Scripts\activate

# Install requirements
pip install -r requirements.txt

# Download required models (see above)
# Place yolov8x.pt in root directory
# Place other models in models/ directory

# Add your input video
# Place your tennis video in input_videos/input_video.mp4
```

## 🚀 Usage

```bash
python main.py
```

The script will:
- Detect players and track their movement
- Track the tennis ball
- Detect court lines and keypoints
- Generate mini court visualization
- Save processed video to output_videos/

---
