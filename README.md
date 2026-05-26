# 🔍 YOLO-COCO-Visual-Search

## 🚀 AIM
Computer Vision Powered Image Search & Real-Time Object Detection using YOLOv11 and the COCO Dataset.

---

# 📖 Abstract

The YOLO Image Search System is a computer vision application built using **YOLOv11** for real-time object detection and intelligent image retrieval. The system detects objects present in images, generates searchable metadata from detection outputs, and enables users to perform visual similarity searches and object-based filtering.

An interactive **Streamlit web interface** allows users to:

- Upload and process images
- Detect objects using YOLOv11
- Visualize bounding boxes
- Generate metadata in JSON format
- Search images using object filters
- Retrieve visually similar images

The project combines:

- Real-time object detection
- Metadata engineering
- Feature extraction & similarity matching
- GPU-accelerated inference
- Deployable web UI

This system demonstrates how modern computer vision techniques can be integrated into an intelligent and scalable image search application.

---

# 🧠 Features

✅ Real-time YOLOv11 object detection  
✅ Visual similarity image search  
✅ COCO dataset support (80 classes)  
✅ Metadata generation using JSON  
✅ Search-by-object-name functionality  
✅ Logical filtering using AND/OR conditions  
✅ Threshold-based search filtering  
✅ Streamlit-based interactive UI  
✅ GPU & CPU support  
✅ Bounding box visualization  
✅ Reusable metadata for faster querying  
✅ Exception handling & logging system  
✅ Supports multiple image formats  

---

# 📂 Dataset & YOLO Model Details

## 📊 COCO Dataset (2017)

The project uses the **COCO 2017 dataset**, containing:

- **118K training images**
- **5K validation images**
- **80 common object categories**

### Example Classes
- person
- car
- dog
- cat
- laptop
- cup
- airplane
- banana

---

# 🤖 YOLOv11 Model

### Model Used
`yolo11m.pt`

### Model Capabilities
- Pretrained on COCO dataset
- Real-time object detection
- Bounding box prediction
- Confidence score prediction
- Fast GPU inference
- Optimized CPU execution

YOLOv11 was selected because of its:

- High detection accuracy
- Faster inference speed
- Real-time performance
- Efficient deployment capability

---

# 🛠️ Environment Setup

## 📌 Prerequisites

Before running the project, install:

- Python 3.10 / 3.11
- Anaconda or Miniconda
- Visual Studio Code
- NVIDIA GPU *(Optional for GPU acceleration)*

---

# 📁 Required Project Files

```bash
app.py
requirements.txt
instructions.txt
src/
models/
dataset/
```

---

# ⚙️ Create Conda Environment

## For Python 3.10

```bash
conda create -n yolosearch python=3.10 -y
conda activate yolosearch
```

## For Python 3.11

```bash
conda create -n yolo-image-search-gpu python=3.11 -y
conda activate yolo-image-search-gpu
```

---

# 📦 Install Dependencies

## Basic Installation

```bash
pip install ultralytics
pip install streamlit
pip install opencv-python
pip install numpy
pip install pillow
```

---

# ⚡ GPU Installation Steps

*(For NVIDIA GPU Users)*

## Step 1 — Install CUDA Toolkit
Recommended Version:
```bash
CUDA 11.8 or CUDA 12.4
```

## Step 2 — Install cuDNN

Install cuDNN compatible with your CUDA version.

---

## Step 3 — Install PyTorch with CUDA Support

### CUDA 11.8

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

### CUDA 12.4

```bash
conda install pytorch torchvision pytorch-cuda=12.4 -c pytorch -c nvidia
```

---

## Step 4 — Install Remaining Requirements

```bash
pip install -r requirements.txt
```

---

# 💻 CPU Installation Steps

If no GPU is available:

```bash
pip install torch torchvision torchaudio
pip install ultralytics
```

---

# 🖥️ How to Run in VS Code using Conda

## Step 1 — Activate Environment

```bash
conda activate yolosearch
```

OR

```bash
conda activate yolo-image-search-gpu
```

---

## Step 2 — Open VS Code Terminal

```text
View → Terminal
```

---

## Step 3 — Select Python Interpreter

Choose the interpreter corresponding to your Conda environment.

---

## Step 4 — Run YOLO Inference Script

```bash
python src/inference.py
```

---

# 🌐 Run Streamlit Application

Launch the web application:

```bash
streamlit run app.py
```

The terminal will display:

```text
Local URL: http://localhost:8501
```

Open the URL in your browser.

---

# 🧩 Streamlit UI Features

The web interface provides:

- Upload image dataset
- Select YOLOv11 model
- Process images
- Detect objects
- Generate metadata
- Apply object filters
- Display result grid
- Perform similarity search
- Export JSON metadata
- Reload previously generated metadata

---

# 🔍 Image Search Pipeline

The project follows this workflow:

```text
Input Image
      ↓
YOLOv11 Object Detection
      ↓
Bounding Box & Class Prediction
      ↓
Metadata Generation (JSON)
      ↓
Feature Extraction
      ↓
Similarity Matching
      ↓
Search & Retrieval Results
```

---

# 🖼️ Output Screenshots


## UI Screenshot
<img width="1919" height="1018" alt="Screenshot 2026-05-26 120107" src="https://github.com/user-attachments/assets/c6282f37-a601-4829-9262-7bb150ad340c" />


## Object Detection Output
<img width="1919" height="1013" alt="Screenshot 2026-05-26 121028" src="https://github.com/user-attachments/assets/41655f15-ae92-40ba-bb49-0fa71919310f" />


<img width="1919" height="1014" alt="Screenshot 2026-05-26 121104" src="https://github.com/user-attachments/assets/7b8bb956-dcc2-4424-a6c1-290f3100c7e8" />


## VS Code Terminal Output
<img width="1919" height="1020" alt="Screenshot 2026-05-26 122322" src="https://github.com/user-attachments/assets/8884fc09-f548-4ed7-97c7-2dec42d47d33" />


## Similarity Search Results
<img width="1918" height="1020" alt="Screenshot 2026-05-26 121128" src="https://github.com/user-attachments/assets/400cbd86-cc40-481a-b8c3-5a0e5b3a02b2" />


---

# 🚀 Enhancements & Innovations

This project extends beyond traditional object detection by integrating:

### 🔹 Metadata-Based Search
Detection outputs are stored as JSON metadata for fast querying without rerunning inference.

### 🔹 Visual Similarity Retrieval
Uses embedding vectors and feature extraction for intelligent image matching.

### 🔹 Logical Filtering
Supports:
- AND conditions
- OR conditions
- Confidence threshold filtering

### 🔹 GPU Acceleration
Optimized for NVIDIA GPU inference using CUDA-enabled PyTorch.

### 🔹 Modular Architecture
The pipeline is modular, scalable, and maintainable for future extensions.

### 🔹 Faster Reusability
Previously generated metadata can be loaded directly to avoid repeated computation.

---

# 📊 Results

## Performance

| Metric | Result |
|---|---|
| Detection Accuracy | High |
| Inference Speed (GPU) | ~20–40 ms |
| Supported Classes | 80 COCO Classes |
| Deployment | Streamlit |
| Search Speed | Fast |
| UI Experience | User-Friendly |

---

# ✅ Conclusion

The YOLO Image Search System successfully demonstrates a powerful combination of:

- Real-time object detection
- Metadata engineering
- Visual similarity search
- Interactive web deployment

Using YOLOv11 and the COCO dataset, the system achieves fast and accurate object detection while enabling intelligent image retrieval through metadata and feature-based similarity matching.

The application is optimized for both CPU and GPU environments and provides a scalable foundation for future computer vision and search-based systems.

---

# 📚 Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core Programming |
| YOLOv11 | Object Detection |
| COCO Dataset | Detection Classes |
| Streamlit | Web UI |
| OpenCV | Image Processing |
| PyTorch | Deep Learning |
| NumPy | Numerical Computation |
| Pillow | Image Handling |
| Conda | Environment Management |

---

# 👨‍💻 Future Improvements

- Add FAISS-based vector search
- Multi-image batch querying
- Webcam live detection
- Cloud deployment
- Mobile-friendly UI
- User authentication system
- Advanced semantic image search

---

# 📌 Author

Developed as a Computer Vision & Image Retrieval Project using YOLOv11 and Streamlit.
