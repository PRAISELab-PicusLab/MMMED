# 🏥 *M*ultilingual *M*ultimodal *M*edical *E*xam *D*ataset for Visual Question Answering in Healthcare
[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

The **Multilingual Multimodal Medical Exam Dataset** (MMMED) is a comprehensive benchmark designed to evaluate Vision-Language Models (VLMs) on _medical multiple-choice question answering (MCQA) tasks_. This dataset combines medical images and multiple-choice questions in **Spanish**, **English**, and **Italian**, derived from the **Médico Interno Residente (MIR)** residency exams in Spain.

The dataset includes challenging, real-world medical content, with images from various diagnostic scenarios, making it ideal for assessing VLMs in cross-lingual medical tasks.

### 🌟 **Key Features**:
- **Languages**: 🇪🇸 Spanish, 🇬🇧 English, 🇮🇹 Italian
- **Medical Content**: Questions based on real Spanish residency exams
- **Image Types**: Diagnostic medical images (e.g., CT scans, X-rays)
- **Categories**: 24 medical specialties (e.g., Digestive Surgery, Cardiology)
- **Multimodal**: Each question comes with a medical image 📸

### 🔄 **Dataset Workflow**
Here is the general workflow for building the MMMED dataset for Vision-Language Model (VLM) evaluation:

![image](https://github.com/user-attachments/assets/94eb7b24-91eb-4221-8ae2-d10f11738505)

### 📊 **Dataset Overview**
The MMMED dataset contains 194 questions from the MIR exams and features images from real-world medical contexts. The dataset is organized into 24 medical categories, each with corresponding textual questions and image-based choices.

| **Statistic**               | **🇪🇸 Spanish** | **🇬🇧 English** | **🇮🇹 Italian** |
|-----------------------------|-----------------|-----------------|----------------|
| **# Questions**             | 194             | 194             | 194            |
| **# Categories**            | 24              | 24              | 24             |
| **Last Update**             | 2024            | 2024            | 2024           |
| **Avg. Option Length**      | 6.85            | 6.57            | 6.71           |
| **Max. Option Length**      | 41              | 39              | 39             |
| **Total Question Tokens**   | 10,898          | 10,213          | 10,545         |
| **Total Option Tokens**     | 5,644           | 5,417           | 5,528          |
| **Avg. Question Length**    | 56.18           | 52.64           | 54.36          |
| **Max. Question Length**    | 223             | 190             | 197            |

### 🖼️ **Image Types**
Categorization of Image Types in the MMMED Dataset. This figure presents the four main categories of images included in the dataset and their respective distributions.

![image](https://github.com/user-attachments/assets/f881f54f-2891-48dd-a6af-90e4844e9c89)

### ✨ **Example MMCQA**
Each multimodal multiple-choice question-answer (MMCQA) pair integrates three essential components with the following structure:
- **Category**: $C$
- **Question**: $Q$
- **Image URL**: $I$
- **Answer Options**: $O$
- **Correct Answer**: 💡

Here’s an illustrative example of multimodal QA in three languages:

![image](https://github.com/user-attachments/assets/7863fc1f-6ef5-41c3-9b8a-31b8429d23d3)

### 🔍 **List of Open-Source and Closed-Source Vision-Language Models (VLMs) Used**
This table shows the parameter sizes, language models, vision models, and average scores of VLMs evaluated on the OpenVLM Leaderboard.

| **Rank** | **Method**               | **Param (B)** | **Language Model**  | **Vision Model**        | **Avg Score (%)** |
|----------|--------------------------|---------------|---------------------|-------------------------|-------------------|
| **Open-Source Models** |
| 167      | PaliGemma-3B-mix-448      | 3             | Gemma-2B            | SigLIP-400M             | 46.5              |
| 108      | DeepSeek-VL2-Tiny        | 3.4           | DeepSeekMoE-3B      | SigLIP-400M             | 58.1              |
| 135      | Phi-3.5-Vision           | 4             | Phi-3.5             | CLIP ViT-L/14           | 53.0              |
| 209      | LLaVA-v1.5-7B            | 7.2           | Vicuna-v1.5-7B      | CLIP ViT-L/14           | 36.9              |
| **Closed-Source Models** |
| 34       | Claude3.5-Sonnet-20241022 | Unknown       | Closed-Source       | Closed-Source           | 70.6              |
| 24       | GPT-4o (1120, detail-high) | Unknown      | Closed-Source       | Closed-Source           | 72.0              |
| 20       | Gemini-2.0-Flash         | Unknown       | Closed-Source       | Closed-Source           | 72.6              |

### 📈 **VLM Performance on MMMED**
The following figure presents the accuracy of different VLMs in each language tested:

![image](https://github.com/user-attachments/assets/6d7b4553-049e-47c0-b0fb-012e78955b91)

### 🔓 **How to Access the Dataset**
You can access the **MMMED** dataset via [Hugging Face](https://huggingface.co/datasets/praiselab-picuslab/MMMED). Follow these steps to download it:

#### Login using e.g. `huggingface-cli login` to access this dataset
```
from datasets import load_dataset

# Login using e.g. `huggingface-cli login` to access this dataset
ds = load_dataset("praiselab-picuslab/MMMED")
```


### 🌐 **Notes**
**Dataset Usage**: The dataset is intended for academic and research purposes only. It is not recommended for clinical decision-making or commercial use.

👨‍💻 This project was developed by Antonio Romano, Giuseppe Riccio, Mariano Barone, Gian Marco Orlando, Diego Russo, Marco Postiglione, and Vincenzo Moscato  
*University of Naples, Federico II*

## 📜 **License**
This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg
