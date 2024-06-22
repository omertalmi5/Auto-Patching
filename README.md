# Auto-Patching: Enhancing Multi-Hop Reasoning in Language Models

**Authors:** Dean Tahory, Omer Talmi, Omar Abo Mokh, Aviv Jan

## Abstract

This repository contains the implementation of the Auto Patch method, a approach that leverages dynamic hidden state patching to enhance the multi-hop reasoning capabilities of LLMs. Using the PatchScopes framework, Auto Patch dynamically adjusts the model’s hidden states during inference to improve its ability to synthesize information across different steps. We evaluated our method on the MuSiQue dataset, focusing on 2-hop questions, and compared its performance against baseline and Chain-of-Thought (CoT) prompting methods. The results show that Auto Patch significantly outperforms the baseline.

## Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
- [Experiments](#experiments)
- [Results](#results)

## Introduction

In recent years, large language models (LLMs) have demonstrated significant advances in natural language understanding and generation. However, these models often struggle with complex reasoning tasks, particularly those involving multi-hop questions that require linking multiple pieces of information. In this project, we introduce the Auto Patch method to enhance the multi-hop reasoning capabilities of LLMs by dynamically adjusting hidden states during inference.

## Methodology

### Data Collection and Preprocessing

We used the MuSiQue dataset, which is designed for evaluating multi-hop reasoning tasks, focusing on 2-hop questions. The data was preprocessed to align with the PatchScopes framework, ensuring that the input formats were standardized.

### Baseline Performance Evaluation

An initial evaluation was conducted using the LLaMA 2 model (7B version) on the MuSiQue dataset.

### PatchScopes Framework Implementation

We used the PatchScopes framework to allow for dynamic adjustment of hidden states during inference. This involved both manual and automated patching processes to refine the model's reasoning capabilities.

### Classifier Training for Auto Patching

A Support Vector Machine (SVM) classifier was trained to automate the patching process. The classifier was trained on features generated from the patching process to predict the optimal positions for patching.

### Auto Patching

Auto Patch dynamically manipulates hidden states at specific positions determined by the classifier to enhance multi-hop reasoning capabilities.

## Experiments

### Evaluation Metrics

- **Accuracy**: The primary metric used to evaluate the performance of the Auto Patch method.
- **Improvement Over Baseline**: Measured the improvement in accuracy achieved by Auto Patch compared to the baseline performance.

### Experimental Setup

Experiments were conducted to compare the performance of Auto Patch with the baseline and Chain-of-Thought (CoT) prompting methods on the MuSiQue dataset.

## Results

| Method               | Accuracy (%) |
|----------------------|--------------|
| Baseline (LLaMA 2)   | 18.45        |
| Chain-of-Thought     | 27.44        |
| Auto Patch (Ours)    | 23.63        |

The Auto Patch method significantly outperformed the baseline, demonstrating its effectiveness in enhancing multi-hop reasoning.
