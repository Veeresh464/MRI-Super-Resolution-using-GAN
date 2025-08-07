# MRI Super-Resolution using GAN

This project implements a Generative Adversarial Network (GAN) to enhance low-resolution MRI brain images into high-resolution images. The objective is to generate high-quality MRI scans to assist in tumor detection and diagnosis, particularly when the original data is noisy or degraded.

---

## 🧠 Project Highlights

- Trained a GAN on paired low- and high-resolution MRI images.
- Evaluated the model on both clean and noisy tumor-affected MRI scans.
- Used preprocessed and filtered datasets to ensure data quality.
- Final trained model included for reuse and evaluation.

---

## 🗂️ Project Structure

```bash
nlp/
│
├── Data/
│   ├── filtered_high/           # High-resolution original MRI images
│   └── filtered_low/            # Low-resolution original MRI images
│
├── largeFiltered/              # Preprocessed MRI images for training (both HR and LR)
│
├── final_model/                # Saved pretrained GAN model
│
├── mri-positive/               # Real MRI images with detected tumors
├── noised-mri-positive/       # Noisy/low-res versions of tumor images
├── generated-positive-mri/    # Output of GAN model on positive cases
│
├── copyof mri2/                # Folder with the main GAN training code
│
└── testing.ipynb               # Final evaluation notebook for pretrained model
│
└── requirements.txt               # Final evaluation notebook for pretrained model
```

🚀 How to Run
1. Clone the Repository
```bash
git clone https://github.com/ManojPandekamat/nlp.git
cd nlp
```

2. Install Dependencies
```bash
pip install -r requirements.txt
```
3. Train the Model (Optional)
```
MRI.ipynb
use a Jupyter Notebook to explore and train interactively.
```
4. Evaluate the Model
```
jupyter notebook testing.ipynb
Compares outputs from generated-positive-mri with real tumor-affected MRI images.
```

🧪 Results
**The model successfully enhances noisy MRI images.**

Generated outputs from generated-positive-mri visually match the original mri-positive set.

Quality gain demonstrated through qualitative evaluation.

🧠 About the Pretrained Model
Located in the final_model/ directory.

Can be directly loaded for inference without retraining.

Works well on unseen noisy tumor images.

# 📌 TODO / Ideas
- Include automatic evaluation metrics (e.g., PSNR/SSIM calculation scripts).
- Build a simple UI for medical professionals to upload low-res scans and view results.
- Use diffusion models or transformers for performance comparison.

```
🤝 Credits
Project by Manoj Pandekamat
Final Year Student | KLE Technological University, Hubballi
```
