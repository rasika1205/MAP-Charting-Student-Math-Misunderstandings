---

# MAP – Charting Student Math Misunderstandings

This repository contains the final notebook submission for the [MAP (Misconception Annotation Project)](https://www.kaggle.com/competitions/math-misconceptions) Kaggle competition. The objective of the competition is to develop a robust NLP-based ML model that accurately predicts student misconceptions from open-ended math explanations.

## 🧠 Competition Overview

In this competition, you are tasked with predicting students’ potential math misconceptions based on their textual explanations for math questions. The goal is not merely to flag correct or incorrect answers but to **identify conceptual misunderstandings** that students might have, even when explanations seem plausible.

These predictions are intended to assist educators in quickly pinpointing widespread misconceptions across students and topics, ultimately enabling **more personalized and effective feedback** to improve math learning outcomes.

The model must generalize to explanations across different math problems — a core challenge of this competition.

---

## 💡 Project Highlights

* ✅ **Final submission includes a powerful ensemble model combining**:

  * **SBERT embeddings** for semantic representation
  * **XGBoost** for capturing non-linear feature interactions
  * **Logistic Regression** for robust probabilistic calibration
* 📊 Thorough **exploratory data analysis** and preprocessing
* 🧪 Deep experiments with alternative models and approaches (not included in the final notebook but were extensively explored)
* 📁 Final model strictly adheres to submission format and evaluation metrics (`MAP@3`)

---

## 🧱 Repository Contents

* `Submission.ipynb` – Final cleaned notebook containing:

  * Data exploration
  * Feature extraction using SBERT
  * Training and ensembling (XGBoost + Logistic Regression)
  * Prediction formatting as per competition specs

---

## ⚙️ Getting Started

To reproduce the notebook:

1. Clone this repository:

   ```bash
   git clone https://github.com/rasika1205/MAP-Charting-Student-Math-Misunderstandings.git
   cd MAP-Charting-Student-Math-Misunderstandings
   ```

2. Install required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. Run `Submission.ipynb` in a Jupyter environment.

> **Note**: The notebook assumes access to the Kaggle dataset. Please ensure that you have accepted the competition rules and have the data in the appropriate path or modify the path accordingly.

---

## 📊 Model Details

### ✨ Sentence Embedding:

* **Model**: [all-MiniLM-L6-v2 (SBERT)](https://www.sbert.net/docs/pretrained_models.html)
* Used to convert student explanations into dense semantic vectors.

### ⚙️ Ensemble Learning:

* **XGBoost**: Captures complex interactions between features.
* **Logistic Regression**: Acts as a calibrated meta-model.
* The outputs from SBERT are passed to both models and predictions are ensembled to generate the final `Category:Misconception` predictions.

---

## 🎯 Evaluation Metric

* **MAP\@3 (Mean Average Precision at 3)**
  The model outputs up to three misconception labels per explanation. The competition uses MAP\@3 to evaluate the quality and order of predictions, rewarding both correctness and confidence ranking.

---

## 🔗 Kaggle Competition

* **Competition**: [Charting Student Misconceptions](https://www.kaggle.com/competitions/charting-student-misconceptions)
* **Goal**: Annotate student math responses with up to 3 most likely misconception labels
* **Metric**: MAP\@3

---

## 🧾 Acknowledgments

* HuggingFace for SBERT model `all-MiniLM-L6-v2`
* Kaggle for the platform and data
* Community notebooks that inspired early experiments

---

## 📌 Notes

This repository only contains the **final notebook** where the complete ensemble model is implemented and evaluated. The model logic is self-contained in this submission and represents the **culmination of multiple iterative experiments**, including TF-IDF baselines, classical ML, and semantic transformer embeddings.

---

## License

This project is **proprietary** and protected by copyright © 2025 Rasika Gautam.

You are welcome to view the code for educational or evaluation purposes (e.g., portfolio review by recruiters).  
However, you may **not copy, modify, redistribute, or claim this project as your own** under any circumstances — including in interviews or job applications — without written permission.

---

## 🧑‍💻 Author

**Rasika Gautam**
*Data Science & AI Enthusiast* | B.Tech MAC, NSUT
[GitHub](https://github.com/rasika1205)
