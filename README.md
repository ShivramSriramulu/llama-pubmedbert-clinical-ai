# 🩺 Clinical Conversation Summarizer + QA System

**Powered by LLaMA + LoRA + PubMedBERT | Real-Time Clinical NLP Pipeline**

---

## ✅ Project Overview
This project builds an end-to-end AI system that:

- Summarizes clinical conversations (e.g., patient-doctor interactions)
- Extracts clinical insights using question answering (QA)

Built using:
- **TinyLLaMA + LoRA** (for Summarization)
- **PubMedBERT** (for Clinical QA)
- **PEFT + CUDA Accelerated Training**

---

## ✅ Why LLaMA for Summarization?
- LLaMA is a powerful instruction-following language model
- Fine-tuned with LoRA + PEFT for efficient summarization
- Generates structured summaries from messy, multi-turn clinical dialogues
- Chosen for its ability to generalize with minimal fine-tuning

## ✅ Why PubMedBERT for QA?
- Pre-trained on biomedical literature (PubMed abstracts)
- Excellent at extractive question answering in the clinical domain
- Enables retrieval of critical insights like symptoms, diagnosis, treatments
- Fills the gap where LLaMA (a generative model) cannot do extraction

## ✅ Why Use LoRA + PEFT?
- LoRA (Low-Rank Adaptation) with PEFT allows fine-tuning large models on limited GPUs
- Reduces training cost by updating only adapter layers, not full model weights
- Crucial for running on consumer GPUs (like RTX 3090/4090)
- Helps achieve real-time inference after fine-tuning

## ✅ Why CUDA & GPU?
- CUDA-enabled GPUs accelerate model fine-tuning and inference
- Without GPU, transformer models would take hours to process
- Enables batching & real-time summarization/QA in deployment

---

## ✅ Real-World Applications
- 🏥 Clinical Documentation Assistants
- 📄 Real-time medical transcription summarization
- 🔍 Automated symptom/diagnosis extraction for EMR/EHR systems
- 🗣️ Conversational AI in healthcare support systems

---

## ✅ Project Pipeline

```
[Raw Clinical Conversation]  
      ⬇  
[TinyLLaMA + LoRA] → Summarization  
      ⬇  
[PubMedBERT QA] → Extract Clinical Insights  
      ⬇  
[CSV/Report/Real-Time API]
```

---

## ✅ Repository Includes:
- Fine-Tuned Model Checkpoints
- Batch Summarization + QA Scripts
- Training Code for TinyLLaMA + LoRA
- PubMedBERT QA Fine-Tuning Pipeline
- Deployment Ready Scripts (for local/Colab)

---

## ✅ How to Use
1. Clone this repo
2. Install dependencies from `requirements.txt`
3. Use `summarize_and_qa.py` for batch processing

---

## ✅ License & Disclaimer
For research and educational purposes only.  
Clinical usage requires regulatory validation.

---

## ✅ Credits
- Meta AI — LLaMA
- Microsoft Research — PubMedBERT
- Hugging Face — Transformers & PEFT 