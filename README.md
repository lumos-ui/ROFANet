# ROFANet: Reliable Occlusion-aware Fine-grained Alignment Network for Text-based Occluded Person Re-Identification

## Overview

ROFANet is a novel cross-modality alignment framework designed for Text-based Person Re-identification (T-ReID) under occluded conditions. This project addresses the challenge of retrieving pedestrian images using natural language descriptions in real-world scenarios where pedestrians are frequently heavily occluded.


<img width="1622" height="863" alt="图片" src="https://github.com/user-attachments/assets/2559ba3b-a627-4a7d-8497-64e659dd941d" />


## Motivation

Text-based Person Re-identification (T-ReID) aims to retrieve pedestrian images according to natural language descriptions. While this task is increasingly important for multimedia content retrieval, most existing T-ReID methods are developed under ideal conditions with little or no occlusion, making them inadequate for real-world applications. ROFANet tackles this limitation by investigating T-ReID under occluded conditions.

## Key Contributions

ROFANet introduces several innovative components to effectively mitigate semantic information loss and matching noise induced by occlusion:

### 1. Semantic-aware Visibility Estimation (SVE) Module
- Leverages cross-modality attention to derive region-level semantic attributions (including body and background)
- Estimates region visibility (unoccluded probability) via response discrepancies
- Suppresses interference from occluded or semantically ambiguous regions

### 2. Part-aware Semantic Guidance (PSG) Module
- Aggregates image patches and text tokens into part-level representations
- Operates under textual semantic guidance
- Enhances fine-grained alignment between visual and textual modalities

### 3. Visibility- and Reliability-aware Weighting Mechanism
- Incorporated during feature alignment
- Prioritizes reliable and visible regions for cross-modality matching
- Improves robustness in occluded scenarios

## Experimental Results

Extensive experiments on three occluded T-ReID benchmarks demonstrate ROFANet's effectiveness:
- **Occluded-CUHK-PEDES**
- **Occluded-ICFG-PEDES**
- **Occluded-RSTPReid**

ROFANet significantly improves retrieval performance under occlusion and achieves competitive results compared with state-of-the-art methods.

## Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/lumos-ui/ROFANet.git
cd ROFANet
pip install -r requirements.txt
```

## Usage

Refer to the documentation and examples in the repository for detailed usage instructions on training and evaluating ROFANet on T-ReID tasks with occlusion.


```

