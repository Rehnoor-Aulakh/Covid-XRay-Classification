
<div align="center">
  <h1>🩺 Chest X-Ray COVID-19 Radiography Project</h1>
  <p>
    <img src="https://img.shields.io/badge/PyTorch-1.9%2B-blue" alt="PyTorch">
    <img src="https://img.shields.io/badge/Python-3.7%2B-green" alt="Python">
    <img src="https://img.shields.io/badge/Dataset-Kaggle-orange" alt="Kaggle">
  </p>
</div>


## 📝 Overview

This project leverages the COVID-19 Radiography Database to classify chest X-ray images into **COVID-19**, **Normal**, and **Viral Pneumonia** categories using PyTorch. The dataset includes images and corresponding lung masks for each class.

---

## 📂 Dataset Structure

```
COVID-19_Radiography_Dataset/
├── COVID/
│   ├── images/
│   └── masks/
├── Lung_Opacity/
│   ├── images/
│   └── masks/
├── normal/
│   ├── images/
│   └── masks/
├── viral/
│   ├── images/
│   └── masks/
└── test/
    ├── COVID/
    ├── normal/
    └── viral/
```

---

## ⬇️ Download Instructions

1. **Via Kaggle (Recommended):**
   - Use the following code in your notebook:
     ```python
     import kagglehub
     path = kagglehub.dataset_download("tawsifurrahman/covid19-radiography-database")
     ```
   - Or download manually from [Kaggle COVID-19 Radiography Database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database).

2. **Copy Dataset to Project Folder:**
   - The notebook will automatically copy the dataset:
     ```python
     import shutil, os
     project_root = os.getcwd()
     target_dir = os.path.join(project_root, "COVID-19 Radiography Database")
     if not os.path.exists(target_dir):
         shutil.copytree(path, target_dir)
     ```

---

## ⚙️ Setup Instructions

1. **Install Python Packages:**
   - Python 3.7 or higher
   - Install required packages:
     ```bash
     pip install torch torchvision numpy matplotlib pillow kagglehub
     ```

2. **Run the Notebook:**
   - Open `main.ipynb` in Jupyter or VS Code.
   - Execute cells in order to:
     - Download and prepare the dataset
     - Create train/test splits
     - Define PyTorch dataset and transformations
     - Train and evaluate models

---

## 📁 Project Structure

- `main.ipynb`: Main notebook for data loading, preprocessing, model training, and evaluation.
- `COVID-19_Radiography_Dataset/`: Contains all image data and masks.

---

## 📚 References

- [Kaggle COVID-19 Radiography Database](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)
- **Please cite the following articles if you use this dataset:**
  - M.E.H. Chowdhury et al., “Can AI help in screening Viral and COVID-19 pneumonia?” IEEE Access, Vol. 8, 2020, pp. 132665 - 132676.
  - Rahman, T. et al., "Exploring the Effect of Image Enhancement Techniques on COVID-19 Detection using Chest X-ray Images." arXiv preprint arXiv:2012.02238.

---

## 💡 Notes

- Ensure you have sufficient disk space for the dataset.
- The notebook uses PyTorch and torchvision for deep learning tasks.
- For more details on the dataset, see `COVID-19_Radiography_Dataset/README.md.txt`.
