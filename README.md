# A³: Towards Advertising Aesthetic Assessment (CVPR 2026)

[![Paper](https://img.shields.io/badge/Paper-CVPR%202026-blue)](#) [![Dataset](https://img.shields.io/badge/Dataset-A³--Dataset-orange)](#)
[![Model](https://img.shields.io/badge/Model-A³--Align-red)](#)
[![Code](https://img.shields.io/badge/Code-Coming%20Soon-green)](#)

> **Status:** The training/inference code, A³-Dataset, and A³-Align model weights are currently being organized and will be released here very soon. Stay tuned! 🚀

This is the official repository for the CVPR 2026 paper **"A³: Towards Advertising Aesthetic Assessment"**. 

To address the subjectivity, lack of scalability, and poor interpretability in current advertising image evaluation, we introduce **A³**, a comprehensive framework. At the heart of this repository is **A³-Align**, a specialized Multimodal Large Language Model (MLLM) trained to master the rules of advertising aesthetics, demonstrating state-of-the-art performance in both quantitative aesthetic judgment and spatial grounding (e.g., promotional iconography).

---

## 🌟 The A³ Framework

Our work provides a complete ecosystem for automated, interpretable, and progressive advertising aesthetic assessment:

* **A³-Law:** A theory-driven, three-stage hierarchical evaluation paradigm inspired by the AIDA marketing model:
  1. **Perceptual Attention:** Image Fidelity, Integration Realism, Professional Polish.
  2. **Formal Interest:** Hue Adaptability, Color Harmonization, Layout Adaptability.
  3. **Desire Impact:** Copywriting Tone, Promotional Iconography, Aesthetic & Advertising Attributes.
* **A³-Dataset:** A large-scale dataset featuring 30K advertising images and 120K instruction-response pairs, richly annotated with multi-dimensional labels and expert-validated Chain-of-Thought (CoT) rationales.
* **A³-Bench:** A comprehensive evaluation suite covering all A³-Law rules, benchmarking 20+ mainstream MLLMs (open/closed-source, "thinking" vs. "non-thinking").
* **A³-Align (This Model):** A multimodal model optimized via Supervised Fine-Tuning (SFT) and Group Relative Policy Optimization (GRPO) with multi-signal rewards to align strictly with the A³-Law.

---

## 🏆 Model Highlights: A³-Align

**A³-Align** is built upon Qwen3-VL-8B-Instruct and heavily fine-tuned using our A³-Dataset. 

* **Tool-Augmented Reasoning:** Capable of autonomously invoking lightweight analytical tools (Hue Analysis, Color Harmonization, DeepSeek-OCR) within its Chain-of-Thought to ensure evidence-based, grounded judgments.
* **Unmatched Spatial Localization:** Radically improves upon existing MLLMs in grounding tasks. Achieves an **mAP of 0.701** in Promotional Iconography localization, more than double the performance of the best closed-source baselines.
* **Fine-grained Subjective Alignment:** Calibrated using continuous score rewards to accurately mirror human aesthetic and advertising impact ratings (achieving SRCC/PLCC of 0.880).
* **Real-World Utility:** Delivers exceptional performance in downstream applications, including **Quality Advertisement Selection** and providing deep, clear **Prescriptive Advertisement Critique**.

---

## 🚀 Getting Started (Coming Soon)

We are finalizing the release of the code and weights. Once public, you will be able to:

1. **Download the A³-Dataset** from HuggingFace.
2. **Load A³-Align** weights for instant advertisement assessment.
3. **Run the training pipeline** (SFT + GRPO) to reproduce our results.

📝 Citation
If you find our work, dataset, or model useful for your research, please consider citing our paper:
