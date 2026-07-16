# 🔖 HindiTales
---

## 📖 Overview

It is an end-to-end multilingual Generative AI project focused on fine-tuning a LLM model for **children's story generation in hindi**.

The project demonstrates a complete LLM adaptation pipeline:

- Building a multilingual dataset
- Translating English stories into Hindi
- Instruction tuning
- Parameter-Efficient Fine-Tuning (LoRA)
- Story generation
- Automatic evaluation using ROUGE metric
- Interactive Gradio demo

The primary objective was to explore how efficiently multilingual LLMs can be adapted for culturally relevant long-form story generation using limited computational resources.

---

# 🎯 Features

- 📚 TinyStories dataset preprocessing
- 🌍 English → Hindi translation using NLLB-200
- 📝 Instruction-following dataset creation
- 🤖 LoRA fine-tuning on Qwen2.5
- 📖 Hindi story generation
- 📊 ROUGE evaluation
- 🧩 Interactive Gradio interface

---

# 🏗️ Project Pipeline

```
TinyStories Dataset
        │
        ▼
English → Hindi Translation
        │
        ▼
Instruction Dataset Creation
        │
        ▼
LoRA Fine-Tuning
(Qwen2.5-Instruct)
        │
        ▼
Hindi Story Generation
        │
        ▼
Evaluation
(ROUGE metric)
        │
        ▼
Gradio Demo
```

---

# 📂 Dataset

The project uses the **TinyStories** dataset as the source.

### Dataset Processing

1. Load TinyStories
2. Translate English stories to Hindi using Meta's **NLLB-200**
3. Convert stories into instruction-response format
4. Fine-tune Qwen2.5 using LoRA

Example instruction:

```text
Write a Hindi children's story for children aged 5–7 about kindness.
```

Example response:

```text
एक समय की बात है...
```

---

# 🤖 Model

**Base Model**

- Qwen2.5-1.5B-Instruct *(or 3B if applicable)*

### Fine-Tuning

- LoRA (PEFT)
- Hugging Face TRL

---

# ⚙️ Tech Stack

- Python
- Hugging Face Transformers
- Hugging Face Datasets
- TRL
- PEFT
- Evaluate
- Gradio
- PyTorch

---

# 📊 Evaluation

The model was evaluated using:

- ROUGE
- Qualitative comparison with the base model

Evaluation metrics were used to compare generated stories with reference stories from the translated dataset.

---

# 🚀 Running the Project

Install dependencies

```bash
pip install -r requirements.txt
```

Launch the notebook

```
HindiTales.ipynb
```

Run all cells sequentially.

---

# 💡 Future Improvements

- Human preference optimization using DPO
- Larger multilingual datasets
- Better Hindi translations using stronger translation models
- Story outline → Story expansion pipeline
- Text-to-Speech integration for audiobook generation
- Fine-tuning larger multilingual LLMs

---

# 📈 Key Learnings

Through this project I gained hands-on experience with:

- Parameter-Efficient Fine-Tuning (PEFT)
- LoRA Fine Tuninig
- Hugging Face ecosystem
- Dataset creation for LLMs
- Multilingual NLP
- Story generation pipelines
- Automatic evaluation of LLM outputs

---
