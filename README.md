Research on Manchu Multi-Font Recognition Based on Structure-Aware Adversarial Reconstruction with Difficult Instance Masking

This repository contains the official PyTorch implementation for our paper. It includes the source code for the TMAR-Net style normalization framework (Stage I) and the downstream OCR domain adaptation (Stage II).

Note: All scripts use the default hyperparameters specified in the paper. For custom configurations, please check the configuration files or use the --help flag.

1. Repository Structure

stage1/: Source code for TMAR-Net. Includes the main network/training script (convnextgan2.py), evaluation scripts (evaluate.py, evaluate_distribution.py), generation script (generate_images.py), and configurations (config.py).

stage2/: Source code for the downstream OCR engine. Includes scripts for domain adaptation/fine-tuning (train_ocr.py) and final word-level sequence testing (test_ocr.py).

requirements.txt: List of dependencies required to run the project.

2. Usage

Stage I: Font Normalization (TMAR-Net)

Training:
python stage1/convnextgan2.py

Flattening Evaluation:
python stage1/evaluate.py

Generate Reconstructed Images:
python stage1/generate_images.py

Stage II: Downstream OCR Adaptation

Domain Adaptation (3-epoch fine-tuning):
python stage2/train_ocr.py

Final Testing:
python stage2/test_ocr.py
