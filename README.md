# 📚 RNNs (Recurrent Neural Networks)
**Big Data Capstone Design Assignment 2: DS Methodology**

## 📑 Table of Contents
1. [Project Background](#1-project-background)
2. [Installation](#2-installation)
3. [Usage](#3-usage)
4. [Example Code](#4-example-code)
5. [Results](#5-results)
6. [References](#6-references)

---

## 1. 📖 Project Background
Before the introduction of RNNs, traditional feedforward neural networks were widely used, but they had limitations in handling sequential data. RNNs were introduced as an innovative solution to overcome these challenges.

---

## 2. ⚙️ Installation
To run this project, you need to install the required libraries and software. Simply use the following command:

```bash
pip install -r requirements.txt

```

---

## 3. 💡 Usage

To run this RNN project, follow these steps:
1. **Download and extract the dataset**
2. **Prepare and preprocess the audio data**
3. **Define and train the RNN model**
4. **Check the prediction results**

---

## 4. 📝 Example Code

Here’s a sample code that demonstrates how to download, extract, and prepare the dataset for voice recognition:

```python
import os
import urllib.request
import tarfile
import librosa
import numpy as np
import tensorflow as tf
from sklearn.model_selection import train_test_split

# Dataset download URL
DOWNLOAD_URL = "http://download.tensorflow.org/data/speech_commands_v0.01.tar.gz"
DATASET_PATH = "data/speech_commands"

def download_and_extract(dataset_url, dest_path):
    if not os.path.exists(dest_path):
        os.makedirs(dest_path, exist_ok=True)
        tar_path = os.path.join(os.getcwd(), "speech_commands.tar.gz")
        urllib.request.urlretrieve(dataset_url, tar_path)
        with tarfile.open(tar_path, "r:gz") as tar:
            tar.extractall(path=dest_path)
        os.remove(tar_path)

download_and_extract(DOWNLOAD_URL, DATASET_PATH)
```

---

## 5. 📊 Results
(Attention. Simple simulation with toy data
The RNN model successfully reduced the loss from **1.3535** to **4.8001e-06** during training, while achieving high accuracy. After testing, the results demonstrated high accuracy with a test loss of **0.0603**, correctly predicting 'Yes' as 'Yes' with a prediction confidence of **94.15%**.

---

## 6. 📚 References

- Vossen, G. (2018). *Data Mining for Business Analytics: Concepts, Techniques, and Applications in R*. Koros Press.
- What are recurrent neural networks (RNNs)?. Built In. (n.d.). [Link to source](https://builtin.com/data-science/recurrent-neural-networks-and-lstm)
