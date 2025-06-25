# Vietnamese Text Error Correction with Transformers

This project presents a deep learning-based solution for **Vietnamese Text Error Correction**, leveraging state-of-the-art Transformer models **ViT5** and **BARTPHO**. It accurately detects and corrects a wide range of real-world Vietnamese text errors.

## 🧠 Supported Error Types
- **Tonal/Diacritic Errors**: e.g. `ma` → `má`
- **Typing Method Errors** (Telex/VNI): e.g. `chuongw trinhf` → `chương trình`
- **Phonetic/Spelling Errors**: e.g. `nỗi buồn` → `lỗi buồn`
- **Structural & Abbreviation Errors**: e.g. `ko` → `không`

## ✨ Key Features
- ✅ Multi-error correction with real-world examples
- 🚀 Fine-tuned models: **ViT5**, **BARTPHO-syllable**
- 📈 Evaluation using **WER**, **CER**, and **Precision/Recall/F1**
- 🔄 Rich **Data Augmentation Pipeline** for synthetic noisy-clean pairs
- 📒 Google Colab-ready, GPU supported

## 🚀 Getting Started

### 1. Requirements
- Google Account + Colab (no local setup needed)
- All required libraries are installed in the notebook via `!pip install`

### 2. Run the Notebook
- Open [`ViT5.ipynb`](source/ViT5.ipynb) or [`Bart.ipynb`](source/Bart.ipynb) in Colab
- Switch runtime to **GPU**: `Runtime -> Change runtime type -> GPU`
- Run the cells step by step:
  - ✅ Configuration
  - 🔄 Data Augmentation
  - 🧠 Model Loading & Training
  - 📊 Evaluation

## ⚙️ Configuration
Configurable classes for easy experimentation:
- `DataConfig`: paths to raw/processed datasets
- `ModelConfig`: HuggingFace model IDs
- `AugmentationConfig`: noise probabilities
- `TrainingConfig`: epochs, batch size, learning rate, etc.

## 📊 Evaluation Metrics
| Model              | WER ↓ | CER ↓ | Precision ↑ | Recall ↑ | F1-score ↑ |
|--------------------|-------|-------|-------------|----------|------------|
| ViT5-base          | 0.206 | 0.060 | 0.308       | 0.584    | 0.403      |
| BARTPHO-syllable   | 0.340 | 0.079 | 0.161       | 0.461    | 0.238      |

As shown, the fine-tuned ViT5 model demonstrated superior performance across most metrics.



## 🤝 Contributing
Contributions, feedback, and ideas are welcome! Feel free to open an issue or pull request.

## 👥 Authors

- **Phạm Huỳnh Tín** – [`522h0150@student.tdtu.edu.vn`](mailto:522h0150@student.tdtu.edu.vn)  
- **Nguyễn Trung Thăng** – [`522h0145@student.tdtu.edu.vn`](mailto:522h0145@student.tdtu.edu.vn)

> 🏫 This project was developed as part of the *Information Technology Project* course at **Ton Duc Thang University**.
