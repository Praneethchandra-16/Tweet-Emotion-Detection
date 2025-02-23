# Tweet-Emotion-Detection
"Fine-tuning transformer models using PEFT and prompt-based learning for tweet emotion detection."
# Tweet Emotion Detection using Transformer Models

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Hugging Face](https://img.shields.io/badge/HuggingFace-Transformers-yellow) ![PEFT](https://img.shields.io/badge/PEFT-LoRA-green)

## 📌 Overview
This project focuses on **multi-label sentiment classification** of tweets using **state-of-the-art Transformer models**. The project evolved through multiple stages, progressively improving **accuracy, efficiency, and computational cost**:

- **HW5**: Custom MLP Model (Baseline)
- **HW6**: Full Fine-Tuning with Transformers (RoBERTa, ALBERT, DistilBERT)
- **HW7**: Parameter-Efficient Fine-Tuning (PEFT) using LoRA & BitsAndBytes
- **HW8**: Prompt-Based Fine-Tuning with PEFT (Meta LLaMA-3.2-1B-Instruct)

🚀 **Final Model:** `Meta LLaMA-3.2-1B-Instruct` with **PEFT + Prompt-Based Tuning**, achieving **51.58% accuracy in optimism detection**.

---

## 🔧 Installation
Ensure you have Python **3.8+** installed. Then, install dependencies:
```bash
pip install torch transformers peft datasets accelerate wandb
```

---

## 📂 Project Structure
```
tweet-emotion-detection/
├── HW5/                  # Custom MLP model
├── HW6/                  # Transformer fine-tuning
├── HW7/                  # PEFT-based fine-tuning
├── HW8/                  # Prompt-based tuning
├── results/              # Submission CSVs & model evaluations
├── models/               # Fine-tuned models (optional)
├── README.md             # Project documentation
```

---

## 🚀 How to Train & Evaluate
Run the training scripts for different methods:
```bash
python train.py --model roberta-base       # HW6 - Full fine-tuning
python train.py --model llama-3.2-1B-peft  # HW7 - PEFT fine-tuning
python train.py --model llama-3.2-1B-prompt # HW8 - Prompt tuning
```

For evaluation:
```bash
python evaluate.py --model best_model
```

---

## 📊 Key Findings
| Approach  | Accuracy | Efficiency |
|-----------|---------|------------|
| **HW5 - MLP**  | 37% | Low  |
| **HW6 - Transformers (RoBERTa)** | 45% | High Compute Cost |
| **HW7 - PEFT (E5-Mistral-7B, Gemma, LLaMA)** | 49% | 55% Lower Cost |
| **HW8 - Prompt Tuning (LLaMA-3.2-1B-Instruct)** | **51.58%** | Most Efficient |

---

## 🤝 Contributing
Feel free to **fork this repo**, submit issues, or contribute with pull requests!

---

## 📜 License
This project is open-source and available under the **MIT License**.

