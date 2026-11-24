
# 🚗 Automatic Number Plate Recognition (ANPR)

An Automatic Number Plate Recognition system built using **Python, YOLO, EasyOCR, OpenCV, and Streamlit**. The application detects number plates from uploaded images and videos, extracts registration numbers using OCR, and tracks detected plates across video frames.

## ✨ Features

- **Vehicle and Number Plate Detection:** Uses YOLO-based pretrained models to detect number plates.
- **Optical Character Recognition (OCR):** Uses EasyOCR to extract text from detected number plates.
- **Video Processing:** Supports video uploads and processes selected frames.
- **Vehicle Tracking:** Uses DeepSORT with SORT/IOU fallback for tracking across video frames.
- **Image Preprocessing:** Applies image enhancement techniques to improve OCR results.
- **Detection Confidence:** Allows users to adjust the detection confidence threshold.
- **CSV Export:** Download recognized number plate results as a CSV file.
- **Interactive Interface:** Simple and user-friendly Streamlit dashboard.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| YOLO | Object and number plate detection |
| EasyOCR | Number plate text recognition |
| OpenCV | Image and video processing |
| Streamlit | Web application interface |
| DeepSORT | Object tracking |
| SORT | Tracking fallback |
| NumPy | Numerical operations |
| Pandas | Result processing and CSV export |
| SciPy | Image processing support |

## 📁 Project Structure

```text
ANPR/
│
├── detectors/
├── models/
│   ├── number_plated/
│   └── vehicle_detection_model/
│
├── recognizers/
├── sort/
├── tracking/
│
├── app.py
├── anpr_config.py
├── easy_ocr.py
├── final_ocr_keras.py
├── utils.py
│
├── yolo11n.pt
├── yolov8n.pt
│
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
└── .gitattributes
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Krish-jain20/Automatic-Number-Plate-Recognition.git
```

```bash
cd Automatic-Number-Plate-Recognition
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
```

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
streamlit run app.py
```

Open the following address in your browser:

```text
http://localhost:8501
```

## 🚀 How to Use

1. Start the Streamlit application.
2. Upload a vehicle image or video.
3. The YOLO model detects potential number plates.
4. The detected plate regions are preprocessed using OpenCV.
5. EasyOCR extracts the registration number.
6. For videos, DeepSORT/SORT tracking maintains object IDs across frames.
7. View the detected number plates and confidence scores.
8. Download the recognition results as a CSV file.

## 🧠 System Workflow

```text
        Input Image / Video
                 |
                 v
        YOLO Detection Model
                 |
                 v
       Number Plate Detection
                 |
                 v
        Image Preprocessing
                 |
                 v
            EasyOCR
                 |
                 v
       Number Plate Recognition
                 |
                 v
        DeepSORT / SORT Tracking
                 |
                 v
        Display Detection Results
                 |
                 v
            CSV Export
```

## 📦 Pretrained Models

The project uses pretrained YOLO model weights stored in the repository.

- `models/number_plated/number_plates_model.pt`
- `models/vehicle_detection_model/best.pt`
- `yolo11n.pt`
- `yolov8n.pt`

These model files are required by the detection pipeline. Keep them in their expected locations.

The repository uses Git LFS for large model files. Install Git LFS before cloning if necessary:

```bash
git lfs install
git clone https://github.com/Krish-jain20/Automatic-Number-Plate-Recognition.git
```

## 📷 Supported Input Formats

**Images:** JPG, JPEG, PNG

**Videos:** MP4, AVI, MOV

## 🔮 Future Improvements

- Improve recognition accuracy under different lighting conditions.
- Support additional regional number plate formats.
- Optimize processing speed for real-time applications.
- Add database integration to store recognized vehicle information.
- Develop a deployment-ready web application.


## 👨‍💻 Author

**Krish Jain**

GitHub: https://github.com/Krish-jain20
