# English-Igbo-Hate-Speech-Detection
Automatic hate speech detection in English-Igbo code-mixed social media data using XLM-RoBERTa.
# Automatic Hate Speech Detection in English–Igbo Code-Mixed Social Media Data Using AI/ML

##  Project Overview

This project focuses on the development of an automatic hate speech detection system for **English–Igbo code-mixed social media data** using Artificial Intelligence and Machine Learning techniques.

The system is designed to classify social media text into four categories:

* **Normal** — non-hateful or ordinary content
* **Offensive** — insulting, abusive, or offensive content that does not necessarily constitute hate speech
* **Hate** — content that expresses hatred, hostility, or promotes discrimination against a person or group
* **Counter** — content that counters, condemns, or responds negatively to hateful or offensive content

The project addresses the challenges associated with processing **code-mixed language**, where users combine English and Igbo within the same social media text.

---

##  Objectives

The main objectives of this project are to:

1. Develop an automated system for detecting hate speech in English–Igbo code-mixed social media text.
2. Preprocess and prepare a labelled dataset for machine learning.
3. Fine-tune a multilingual transformer model for text classification.
4. Classify texts into normal, offensive, hate, and counter-speech categories.
5. Evaluate the performance of the trained model using standard classification metrics.
6. Demonstrate the application of AI/ML techniques to multilingual and code-mixed social media data.

---

##  Dataset

The dataset contains social media text labelled according to the following categories:

| Label       | Description                                               |
| ----------- | --------------------------------------------------------- |
| `normal`    | Non-hateful or ordinary content                           |
| `offensive` | Offensive or abusive content                              |
| `hate`      | Hate speech or hateful content                            |
| `counter`   | Counter-speech directed against hateful/offensive content |

The dataset is divided into:

* **Training set**
* **Validation set**
* **Test set**

The dataset contains English–Igbo code-mixed content, making it suitable for investigating hate speech detection in multilingual social media environments.

> **Note:** The dataset itself is not included in this repository where redistribution or publication of the original data is not permitted.

---

##  Data Preprocessing

The preprocessing stage prepares the raw text for model training.

The process includes:

* Loading the dataset using Pandas
* Checking the dataset structure
* Handling missing text values
* Preparing the text and label columns
* Converting categorical labels into numerical representations
* Maintaining the predefined training, validation, and test splits
* Preparing the text for tokenization

The preprocessing is performed before the data is passed to the transformer model.

---

##  Model

The project uses **XLM-RoBERTa (XLM-R)** for multilingual text classification.

XLM-RoBERTa is a multilingual transformer model designed to work with text in many languages. Its multilingual capabilities make it appropriate for this project because the dataset contains both **English and Igbo**, sometimes within the same sentence.

The pretrained XLM-RoBERTa model is fine-tuned for a **four-class sequence classification task**.

### Classification Architecture

```text
Input Social Media Text
          ↓
      Tokenization
          ↓
     XLM-RoBERTa
          ↓
 Classification Head
          ↓
 ┌────────┬───────────┬──────┬─────────┐
 │ Normal │ Offensive │ Hate │ Counter │
 └────────┴───────────┴──────┴─────────┘
```

---

##  Technologies Used

* **Python**
* **Google Colab**
* **PyTorch**
* **Hugging Face Transformers**
* **Hugging Face Datasets**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **XLM-RoBERTa**

---

##  Model Training

The pretrained XLM-RoBERTa model is fine-tuned using the labelled dataset.

The training pipeline consists of:

1. Loading the dataset
2. Preparing the labels
3. Tokenizing the text
4. Creating training, validation, and test datasets
5. Loading the pretrained XLM-RoBERTa model
6. Fine-tuning the model on the training data
7. Evaluating performance using the validation data
8. Testing the final model on unseen test data

The trained model and tokenizer can be saved for later inference.

---

##  Evaluation

The model is evaluated using standard machine-learning classification metrics, including:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**

These metrics provide different perspectives on how well the model distinguishes between normal, offensive, hate, and counter-speech content.

The test set is kept separate from the training process and is used to evaluate the model on unseen examples.

---

##  Prediction

After training, the model can be used to classify new English–Igbo code-mixed social media text.

Example:

```python
text = "Example English–Igbo social media text"

prediction = predict(text)

print(prediction)
```

The system returns one of the four supported classes:

```text
normal
offensive
hate
counter
```

---

##  Repository Contents

```text
English-Igbo-Hate-Speech-Detection/
│
├── hate_speech_detection.ipynb
├── README.md
└── requirements.txt
```

### `hate_speech_detection.ipynb`

Contains the complete implementation of the project, including:

* Data loading
* Data preprocessing
* Tokenization
* Model configuration
* XLM-RoBERTa fine-tuning
* Model evaluation
* Prediction

---

##  Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/English-Igbo-Hate-Speech-Detection.git
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

The project can be run using:

* Google Colab
* Jupyter Notebook
* JupyterLab
* PyCharm with Jupyter support

### 4. Provide the dataset

Place the dataset in the appropriate location and update the dataset path in the notebook if necessary.

### 5. Run the notebook

Execute the cells sequentially to preprocess the data, train the model, evaluate it, and perform predictions.

---

##  Limitations

The project has several limitations:

* Code-mixed English–Igbo text can be difficult to interpret because users may switch languages within a sentence.
* Social media language often contains slang, abbreviations, emojis, spelling variations, and informal expressions.
* The meaning of some statements can depend heavily on context.
* Classification performance depends on the quality, size, diversity, and labelling consistency of the dataset.
* A model trained on one dataset may not generalize perfectly to different social media platforms or communities.

---

##  Future Improvements

Future development could include:

* Increasing the size and diversity of the English–Igbo dataset.
* Improving the representation of Igbo linguistic patterns.
* Investigating additional multilingual transformer models.
* Exploring ensemble and hybrid machine-learning approaches.
* Improving handling of slang, emojis, abbreviations, and spelling variations.
* Developing a real-time hate speech detection application.
* Deploying the trained model as a web API or application.
* Continuously evaluating the model on newly collected code-mixed social media data.

---

##  Academic Project

This repository contains the implementation of an academic project titled:

**"Development of Automatic Hate Speech Detection in English–Igbo Code-Mixed Social Media Data Using AI/ML."**

The project demonstrates the application of Natural Language Processing, Machine Learning, and multilingual transformer models to automated hate speech detection.

---

##  Author

**Vendetta-ops-cy**

Computer Science / Information Technology Project

---

##  License

This project is intended primarily for academic and research purposes.

The availability and redistribution of the dataset are subject to the terms and conditions associated with its original source.
