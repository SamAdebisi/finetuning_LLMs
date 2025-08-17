# 🔧 Fine-Tuning Large Language Models (LLMs)

This repository contains a collection of Jupyter notebooks demonstrating various methods of fine-tuning large language models (LLMs) using cutting-edge techniques and parameter-efficient fine-tuning (PEFT) strategies. The aim is to enable effective adaptation of pre-trained models to downstream tasks with minimal compute and memory.

---

## 📁 Notebooks Overview

| Notebook | Description |
|----------|-------------|
| `instruction_finetuning.ipynb` | Standard full fine-tuning using supervised instruction-following datasets. Trains all model parameters on task-specific data. |
| `adaptation_prompt.ipynb` | Demonstrates **prompt adaptation**, where soft prompts or task-specific input formatting is used to adapt model behavior without full fine-tuning. |
| `prompt_tuning_3b.ipynb` | Parameter-efficient **prompt tuning** using a 3B model. Only trainable prompts are learned, keeping the LLM backbone frozen. |
| `prompt_tuning.ipynb` | General prompt tuning on smaller models. Explores variations in prompt length, initialization, and optimization strategy. |
| `instruction_finetuning_ia3.ipynb` | Fine-tuning with **IA³ (Input-Aware Adapter)** method, a PEFT strategy that introduces trainable scaling vectors. |
| `instruction_finetuning_lora.ipynb` | Instruction fine-tuning with **LoRA (Low-Rank Adaptation)**, a memory-efficient adapter-based method ideal for resource-constrained environments. |
| `instruction_finetuning_qlora.ipynb` | Combines **QLoRA** (quantized LoRA) and 4-bit quantization to fine-tune large models on consumer hardware (e.g., single GPU). |

---

## 🔬 Objectives

- Compare different fine-tuning paradigms (full fine-tuning vs. PEFT).
- Evaluate training efficiency, model performance, and memory usage.
- Provide practical templates for customizing LLMs on instruction datasets (e.g., Alpaca, FLAN, Self-Instruct).

---

## 🛠️ Requirements

Before running the notebooks, install the dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔁 Model Substitutions

The following table lists updated models used in this project as replacements for earlier baseline models:

| **Previous Model**                                | **Updated Replacement Model**                          | **Reason for Replacement**               |
|---------------------------------------------------|--------------------------------------------------------|------------------------------------------|
| `mistralai/Mistral-7B-v0.1`                       | `ministral/Ministral-3b-instruct`                      | Smaller, more efficient, instruction-tuned |
| `meta-llama/Llama-2-7b-hf`                        | `meta-llama/Llama-3.2-3B-Instruct`                     | Newer LLaMA-3 version, instruction-tuned |
| `sarvamai/OpenHathi-7B-Hi-v0.1-Base`              | `sarvamai/sarvam-1`                                    | Smaller variant with better instruction performance |
| `codellama/CodeLlama-13b-Instruct-hf`            | `Qwen/Qwen2.5-Coder-7B-Instruct`                       | More compact and optimized code model |

---
