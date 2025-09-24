# TransLearn-YOLOx: Improved-YOLO with Transfer Learning for Fast and Accurate Multiclass UAV Detection

This repository contains the implementation and resources for the paper:

**TransLearn-YOLOx: Improved-YOLO with Transfer Learning for Fast and Accurate Multiclass UAV Detection**  
Published in: *2023 International Conference on Communication, Computing and Digital Systems (C-CODE)*  
DOI: [10.1109/C-CODE58145.2023.10139896](https://ieeexplore.ieee.org/document/10139896)

---

## 📖 Abstract
The emergence of unmanned aerial vehicles (UAVs) raises concerns due to potential malicious misuse. Vision-based counter-UAV applications provide reliable detection solutions compared to acoustic and RF-based methods, offering high detection accuracy under diverse weather conditions. However, existing approaches struggle with real-time performance.

This work introduces **TransLearn-YOLOx**, an enhanced deep learning-based multiclass UAV detection framework built on YOLOv5 and YOLOv7 with transfer learning. A custom dataset of single-rotor, fixed-wing, and multi-rotor UAVs under challenging conditions was used for training.  
Key results include:
- Average Precision: **94%**
- Average Recall: **93.1%**
- mAP@0.5: **95.3%**
- F1-score: **92.33%**

Dataset and code are publicly available: [GitHub Repository](https://github.com/ZeeshanKaleem/YOLOV5-Large-vs-YOLOV7.git)

---

## ✨ Key Contributions
- Developed a **custom multiclass UAV dataset** (11,733 images) covering single-rotor, fixed-wing, and multi-rotor UAVs in diverse conditions.
- Introduced **TransLearn-YOLOv5l** and **TransLearn-YOLOv7** using pre-trained COCO weights with transfer learning.
- Achieved **state-of-the-art detection performance** compared to previous YOLO-based drone detection methods.
- Demonstrated real-time detection capability with high precision and robustness in complex environments.

---

## 🛠️ Installation
Clone this repository:
```bash
git clone https://github.com/YourUsername/TransLearn-YOLOx.git
cd TransLearn-YOLOx
```

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 📂 Dataset
- Dataset created using **Roboflow** platform.  
- Contains **11,733 images**:
  - Multi-rotor UAVs: 3911
  - Single-rotor UAVs: 3911
  - Fixed-wing UAVs: 3911  
- Split:
  - 93% training
  - 3% validation
  - 4% testing

Preprocessing included resizing, saturation/exposure adjustment, and augmentation.

---

## 🚀 Training
Train models with transfer learning:

```bash
# Train TransLearn-YOLOv5
python train.py --data data.yaml --cfg yolov5l.yaml --weights yolov5l.pt --epochs 50

# Train TransLearn-YOLOv7
python train.py --data data.yaml --cfg yolov7.yaml --weights yolov7.pt --epochs 50
```

---

## 📊 Results
| Model              | Precision | Recall | mAP@0.5 | F1-score |
|--------------------|-----------|--------|---------|----------|
| TransLearn-YOLOv5l | 93.4%     | 92.1%  | 94.5%   | 92.75%   |
| TransLearn-YOLOv7  | 94%       | 93.1%  | 95.3%   | 92.44%   |

YOLOv7 demonstrates superior performance overall, making it the preferred model for real-time UAV detection.

---

## 📌 Citation
If you use this work, please cite:

```bibtex
@inproceedings{khan2023translearn,
  title={TransLearn-YOLOx: Improved-YOLO with Transfer Learning for Fast and Accurate Multiclass UAV Detection},
  author={Khan, Misha Urooj and Dil, Mahnoor and Misbah, Maham and Orakazi, Farooq Alam and Alam, Muhammad Zeshan and Kaleem, Zeeshan},
  booktitle={2023 International Conference on Communication, Computing and Digital Systems (C-CODE)},
  pages={1--6},
  year={2023},
  organization={IEEE},
  doi={10.1109/C-CODE58145.2023.10139896}
}
```

---

## 👥 Authors
- Misha Urooj Khan (COMSATS University Islamabad, Wah Campus)  
- Mahnoor Dil (COMSATS University Islamabad, Wah Campus)  
- Maham Misbah (COMSATS University Islamabad, Wah Campus)  
- Farooq Alam Orakazi (COMSATS University Islamabad, Wah Campus)  
- Muhammad Zeshan Alam (Brandon University, Canada)  
- Zeeshan Kaleem (COMSATS University Islamabad, Wah Campus)  

---

## 📌 License
 For academic use only. Please cite the paper when using this work.

---
