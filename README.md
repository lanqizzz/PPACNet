# PPACNet

## Improving Few-Shot Industrial Surface Defect Segmentation through Progressive Inference Calibration

Official repository for **PPACNet (Progressive Proxy–Affinity Calibration Network)**, an inference-stage calibration framework for few-shot industrial surface defect segmentation.

## Overview

Few-shot industrial surface defect segmentation remains challenging because limited support samples can provide unreliable evidence, query responses may become fragmented in repetitive textures, and the final decision boundary can vary across episodes.

PPACNet addresses these issues through progressive inference calibration while keeping the visual representation frozen.

The framework contains three complementary stages:

- **PPF – Proxy-Prototype Fusion**  
  Organizes foreground, hard-negative, and background evidence with reliability-aware K-shot aggregation.

- **SD-PAC – Support-Driven Patch-Affinity Calibration**  
  Constructs a support-driven response and exploits sparse query self-affinity to improve spatial consistency.

- **EADC – Episode-Aware Decision Calibration**  
  Uses support-side statistics to calibrate the final discrete segmentation decision.

PPF, SD-PAC, and EADC introduce **no additional learnable parameters**.

## Framework

The overall framework of PPACNet is shown below.

![PPACNet Framework](assets/PPACNet_Framework.png)

## Datasets

PPACNet is evaluated on two public few-shot industrial surface defect segmentation benchmarks:

- **FSSD-12**
- **Surface Defects-4i**

Experiments follow the standard three-fold 1-way 1-shot and 5-shot protocols.

## Main Results

### ResNet-50

| Dataset | 1-shot mIoU | 5-shot mIoU |
|---|---:|---:|
| FSSD-12 | 64.35 | 67.36 |
| Surface Defects-4i | 46.14 | 49.89 |

The experiments show that support-evidence organization provides the dominant improvement, while affinity propagation and episode-aware decision calibration contribute complementary gains.

## Code Release

The source code and complete reproduction instructions are currently being organized and will be released in this repository.

## Citation

Citation information will be updated after publication.

## Contact

For questions regarding this work, please open an issue in this repository.
