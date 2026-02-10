# 🌐 Deep Learning Model Benchmarking Project

## 📌 Overview
This project benchmarks multiple deep learning models (solo and combinations) on a shared dataset.  
The goal is to train, evaluate, and compare performance across architectures such as **YOLOv12**, **Swin Transformer**, **UNet**, **MobileNet**, and advanced combinations (UNet + DenseNet, Swin + ViT, CNN + CRF, etc.).

---

## 📂 Project Structure
project_root/
├── data/                # Dataset (train/val/test splits)
├── models/              # Model implementations
│   ├── solo/            # Individual models
│   └── combinations/    # Hybrid/combined models
├── results/             # Checkpoints, metrics, logs
├── utils/               # Shared scripts (dataset loader, metrics, visualization)
└── comparison/          # Aggregated results and comparison scripts

---

## 🚀 Setup

### 1. Clone the Repository
```
git clone <your-repo-url>
cd project_root
```
###2. Create Virtual Environment (Local)
```
python3 -m venv venv
source venv/bin/activate
```
###3. Install Dependencies
```
pip install -r requirements.txt
```
###4. Google Colab Users
Mount Google Drive:
```
from google.colab import drive
drive.mount('/content/drive')
```
Install requirements:
```
!pip install -r /content/drive/MyDrive/Project_Data/requirements.txt
```

###🧑‍🤝‍🧑 Collaboration
Dataset stored in Google Drive (Project_Data/data/).

Each team member trains assigned models using their own account (local VS Code or Colab).

Results (checkpoints + metrics) are saved in results/ and pushed to GitHub (use Git LFS for large files).


📊 Results Comparison
Each model saves metrics (metrics.json) in its results folder.
Run:
```
python comparison/compare_results.py
```

###🔑 Notes

- **Solo models**: `yolov12`, `swin_transformer`, `unet`, `mnet`
  
- - **Combination models**:  
  `unet_densenet`,  
  `unet_resnet`,  
  `attention_se_cbam_unet`,  
  `transferlearning_swintransformer`,  
  `swin_vit`,  
  `attention_se_cbam_unet_swin_vit`,  
  `cnn_crf`,  
  `cnn_mrf`,  
  `deeplabv3_crf`,  
  `unet_densecrf`,  
  `resnet_unet_efficient`

- **Checkpoints** are stored in:  
  `results/[model]/checkpoints/`


