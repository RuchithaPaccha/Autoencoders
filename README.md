# 🧠 Autoencoder for MNIST + Custom Character ("R") Reconstruction

This project demonstrates how an **autoencoder** can learn to reconstruct both standard handwritten digits from the **MNIST dataset** and a **custom handwritten character (letter "R")**. It showcases deep learning's adaptability to new data through preprocessing, reconstruction using a pretrained model, and retraining the autoencoder on extended datasets.

---

## 🔍 Overview

- **Frameworks**: TensorFlow, Keras, NumPy, Matplotlib
- **Task**: Integrate 5 grayscale images of the letter "R" into the MNIST dataset.
- **Goal**: Train an autoencoder to reconstruct both MNIST digits and the custom character using unsupervised learning.
- **Model**: Fully connected autoencoder with 16-dim bottleneck layer.

---

## 📂 File Summary

- `Assignment11_Autoencoders_Ruchitha.ipynb` – Main notebook  
- `initially_trained_autoencoder.h5` – Pretrained autoencoder  
- `R1.png` to `R5.png` – Custom grayscale character images  
- `README.md` – This summary

---

## ⚙️ Key Steps

1. **Preprocessing**:
   - MNIST images reshaped from `(28, 28)` to `(784,)`
   - Normalized to range [0, 1]
   - Custom "R" images resized and converted to grayscale

2. **Reconstruction with Pretrained Model**:
   - Loaded `.h5` model
   - Reconstructed test digits visually (side-by-side comparison)

3. **Custom Character Integration**:
   - Loaded images: `R1.png` to `R5.png`
   - Reshaped and normalized
   - Oversampled to match MNIST dataset size

4. **Model Summary**:
   - Encoder: 784 → 500 → 300 → 100 → 16
   - Decoder: 16 → 100 → 300 → 500 → 784
   - Params: ~1.15M

5. **Training**:
   - Used EarlyStopping
   - Trained on combined dataset (digits + oversampled R)

---

## 📊 Visual Results

- **Top Row**: Original MNIST digits
- **Bottom Row**: Reconstructed outputs
- **Final Output**: Autoencoder successfully reconstructed both digits and "R"

> 🖼️ Conclusion: The model generalized well and visually replicated both digits and the unseen letter "R" — showcasing autoencoder flexibility for custom data integration.

---

## 👩‍💻 Author

**Ruchitha Paccha**  
📧 ruchitha1904@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/ruchitha-chowdary-paccha/)

---

## 🚀 How to Run

```bash
git clone https://github.com/yourusername/autoencoder-mnist-custom.git
cd autoencoder-mnist-custom
jupyter notebook Autoencoders_Ruchitha.ipynb
