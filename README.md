# Unsupervised Clustering of Multilingual Music via Variational Autoencoder Representations


## Overview

This project implements a Universal Variational Autoencoder (UniversalVAE) to cluster hybrid music datasets (English/Bengali). The goal is to investigate if deep generative models can disentangle Genre (acoustic features) from Language (semantic features) without supervision.

## Key Features:

Easy Task: Audio-only VAE vs. PCA Baseline.

Medium Task: Hybrid (Audio+Lyrics) CNN-VAE vs. Advanced Clustering.

Hard Task: Disentangled Representation Learning using Beta-VAE.


## Setup

Clone repo: git clone <repo-link>

Install deps: pip install -r requirements.txt

Add data to data/audio and data/lyrics.

## Usage

Open notebooks/exploratory.ipynb. Change TASK_MODE at the top to run specific tasks:

TASK_MODE = "EASY" (Audio Baseline)

TASK_MODE = "MEDIUM" (Hybrid Clustering)

TASK_MODE = "HARD" (Beta-VAE Disentanglement)

## Results Summary

Easy: VAE outperformed PCA (Silhouette 0.52 vs 0.29), finding latent acoustic structures.

Medium: K-Means proved most robust for latent clustering (Silhouette 0.46).

Hard: Aggressive feature scaling ($W_{text}=500$) successfully disentangled language (Purity 0.85) from genre.
