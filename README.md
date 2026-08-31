# Cryptognosis
A privacy-preserving, multi-institution machine learning system for polygenic disease-risk prediction. Designed to address population stratification across India's founder populations, this system is prototyped using the 1000 Genomes Project South Asian cohorts (PJL, GIH, ITU, STU, BEB)

## Overview

Traditional federated learning methods such as **FedAvg** treat participating clients similarly, which can be problematic when hospitals serve genetically distinct populations.

This project proposes an **ancestry-aware aggregation method** that:

* Generates privacy-preserving ancestry signatures locally.
* Calculates continuous ancestry-based mixture weights.
* Aggregates local models using these weights instead of simple averaging.
* Tracks prediction performance across populations to identify fairness gaps.
* Supports admixed populations through soft rather than rigid ancestry assignment.

## Dataset

The proof of concept uses **1000 Genomes Project Phase 3**, focusing on five South Asian populations:

* PJL — Punjabi
* GIH — Gujarati
* ITU — Telugu
* STU — Sri Lankan Tamil
* BEB — Bengali

Chromosome 22 or a curated SNP panel is used for the prototype.

Since 1000 Genomes does not contain disease phenotypes, **height** is used as a benchmark polygenic trait.

## Experiments

The project compares:

1. Single-site training
2. Centralized training
3. Standard FedAvg
4. **Proposed Ancestry-Weighted Federated Learning**

Performance is evaluated both globally and across individual populations.

## Tech Stack

**Python · Flower · PLINK2 · pandas · NumPy · scikit-learn · PyTorch · YAML · MLflow**

## Project Status

🚧 **Research Prototype**

The current implementation focuses on validating ancestry-aware federated aggregation using simulated institutional nodes. Secure aggregation, differential privacy, and production deployment mechanisms are planned as future work.

## Disclaimer

This is a research prototype and **not a clinically validated disease-risk prediction system**.
