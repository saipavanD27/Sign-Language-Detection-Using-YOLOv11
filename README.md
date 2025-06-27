# Real-Time Detection of Sign Language Gestures Using YOLOv11

This project focuses on the **real-time detection of American Sign Language (ASL)** gestures using the **YOLOv11** object detection model. It aims to bridge the communication gap between hearing-impaired individuals and the general population through advanced computer vision and deep learning technologies.

## 🔍 Overview

Sign language is a vital mode of communication for individuals with hearing or speech impairments. This project leverages YOLOv11 to detect and recognize ASL signs, enabling real-time translation of gestures into readable text. 

### Key Features:
- Detection of ASL alphabets (A–Z) and common gestures like "Hello", "Thanks", "Yes", "No", "Please", "I Love You".
- Real-time object detection using YOLOv11.
- Bounding box annotation for gesture localization.
- Achieved **mAP@0.5: 96.8%** and **mAP@0.5:0.95: 80.9%**.
- Fast inference: ~15ms per image on GPU.

---

## 📁 Dataset

- **Source**: [Roboflow Public Dataset - American Sign Language Letters](https://public.roboflow.com/object-detection/american-sign-language-letters)
- **Description**: Images labeled with bounding boxes for hand signs representing ASL characters and gestures.
- **Total Images**: ~2000
- **Split**:
  - Training: 85%
  - Validation: 10%
  - Testing: 5%

---

## 🛠️ Technologies Used

- **YOLOv11 (You Only Look Once)** for object detection.
- **Python** and **PyTorch** for model training and inference.
- **OpenCV** for image handling.
- **Roboflow** for data preprocessing and annotation.
- **Jupyter Notebook** for prototyping.

---

## 🚀 How to Run

1. Clone the repository.
2. Set up the environment:
    ```bash
    pip install -r requirements.txt
    ```
3. Download the dataset from Roboflow and structure it in YOLO format.
4. Train the model (if needed):
    ```bash
    yolo task=detect mode=train model=yolov11l.pt data=data.yaml epochs=50 imgsz=640
    ```
5. Run detection:
    ```bash
    yolo task=detect mode=predict model=best.pt source=your_image.jpg
    ```

---

## 📊 Results

| Metric       | Value     |
|--------------|-----------|
| mAP@0.5      | 96.8%     |
| mAP@0.5:0.95 | 80.9%     |
| Precision    | 95.3%     |
| Recall       | 92.5%     |

The model performs exceptionally well across most gesture classes, including alphabets and common phrases. Real-time performance was confirmed with inference times under 20ms per frame on GPU.

---

## 🧠 Model Comparison

| Feature                 | CNN     | YOLOv11 |
|------------------------|---------|---------|
| Real-Time Detection    | ❌ No   | ✅ Yes  |
| Gesture Localization   | ❌ No   | ✅ Yes  |
| Multi-Hand Detection   | ❌ No   | ✅ Yes  |
| Accuracy               | High    | Very High |
| Inference Speed        | Slow    | Fast    |

---

## 🙌 Authors

- Donga Saipavan 
- Immaraju Srilekha
- G. Abhishikth
- R Eswar Naik

Department of Computer Science and Engineering,  
IIIT Dharwad, India

---

## 📄 License

This project is for educational and research purposes only.

---

## 🔗 Acknowledgements

- Dataset provided by [Roboflow](https://public.roboflow.com/object-detection/american-sign-language-letters).
- Inspired by ongoing research in gesture recognition and real-time object detection using deep learning.

