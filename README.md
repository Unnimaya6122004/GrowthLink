<a href="#">
  <img align="left" 
       alt="React" 
       width="100%" 
       style="padding-right:10px;" 
       src="https://capsule-render.vercel.app/api?type=waving&height=250&color=0:1a0e05,11:281506,22:381d09,33:48270b,44:57300d,55:663912,66:754216,77:844c1b,88:95541f,99:a65e22,100:a65e22&text=Welcome%20to%20my%20Project&reversal=true&section=header&fontAlignY=45&fontSize=40&textBg=false&animation=twinkling&fontColor=FFFFFF" />
</a>

# ✍️ DeepWriting - Handwriting Stroke Generation with LSTM

This project demonstrates how to **train an LSTM-based model** to generate handwriting strokes from the **DeepWriting dataset**.

The model is trained to predict sequences of pen movements (dx, dy, pen-state).

---

## 📂 Dataset

- **Source**: External ZIP file containing `.npz` files.
- Each `.npz` file contains:
  - `strokes` (list of sequences)
  - `min`, `max` (for normalization).

> Make sure you have your dataset zip file ready:  
> Example filename: `deepwriting_dataset.zip`

---

## 🚀 How to Run (in Google Colab)

### 1. Upload the Dataset

- Upload your `deepwriting_dataset.zip` to the Colab session.
- Or use `files.upload()` in Colab to upload manually.

```python
from google.colab import files
files.upload()  # Select your deepwriting_dataset.zip file
```

---

### 2. Run the Code

Paste and run the entire notebook code provided (split into cells if needed):

- Install packages (`torch`, `torchvision`, `pandas`, `matplotlib`)
- Unzip the dataset
- Load the `.npz` data
- Normalize strokes
- Prepare padded sequences
- Build and train the LSTM model
- Evaluate predictions and plot generated handwriting strokes

---

## 🛠 Project Structure

| Step | Description |
|:----:|-------------|
| 1 | Install dependencies |
| 2 | Unzip and load the dataset |
| 3 | Preprocess: normalize strokes |
| 4 | Create datasets and dataloaders |
| 5 | Define LSTM model |
| 6 | Train and validate the model |
| 7 | Save and load the trained model |
| 8 | Test: generate handwriting strokes |
| 9 | Plot actual vs predicted strokes |

---


## 🧹 Important Notes

- The dataset is **not** a CSV file but an `.npz` file containing arrays.
- Pen-state accuracy is separately calculated.
- The task is treated like a **sequence-to-sequence regression** problem.
- The code automatically uses **GPU** if available.

---

## 📜 Requirements

- Python 3.8+
- PyTorch
- Numpy
- Matplotlib
- Pandas

*(All installed automatically in Colab)*

---

## 📢 Future Improvements

- Add Teacher Forcing during training
- Generate longer freehand strokes
- Fine-tune hidden size, layers for better prediction
- Build a simple Streamlit app for live demo

---

## 🧑‍💻 Author

- ✨ Built with ❤️ by [UNNIMAYA K](https://github.com/Unnimaya6122004)

<a href="#"><img align="left" alt="Finish" width="100%" style="padding-right:10px;" src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:331a00,11:4a2d11,22:5f4025,33:704f38,44:8b6946,55:a5815b,66:c29a73,77:d7b08b,88:e5c8a1,99:f0d9b7,100:f0d9b7&section=footer" /></a>

