# 📦 Catalog Clustering

This project presents an unsupervised multimodal clustering pipeline that organizes thousands of fashion and gifting products (e.g., mugs, T-shirts, bags) into semantically coherent groups. It leverages multimodal embeddings, density-based clustering, and large language models to generate interpretable, scalable cluster outputs suitable for downstream business applications.

---

## ✅ Problem Statement

Our catalog contained thousands of diverse products with associated images and textual metadata. Existing heuristics used for grouping were brittle and not scalable across different categories. The objective was to build a robust, scalable, and interpretable clustering system that could:

- Group visually and semantically similar products.
- Adapt to different category characteristics (e.g., mugs vs. apparel).
- Provide meaningful cluster names to support navigation, tagging, and personalization.

---

## 🧠 Solution Overview

### 🔍 Embedding Generation

We evaluated multiple pre-trained models:
- **FLAVA** (selected): For high-quality multimodal (image + text) embeddings.
- **Merlin** (baseline): Used for comparison.

### 📊 Clustering

- **HDBSCAN** was chosen over KMeans for its ability to find clusters of varying densities without needing to predefine `k`.

### 🏷️ Cluster Naming

- **WordMap**: Frequency-based term extraction from product metadata.
- **LLaMA-2**: Prompt-engineered LLM for generating human-readable cluster names.

### 📈 Evaluation & Visualization

- **Qualitative Evaluation**: Checked intra-cluster coherence and semantic relevance.

---

## ✨ Results

- Achieved semantically consistent clusters (e.g., "festival gift mugs" vs "personalized mugs").
- **FLAVA** outperformed **Merlin** in cluster coherence due to its superior multimodal understanding.
- Cluster naming automation saved internal teams hours of manual effort.
- The pipeline is under consideration for integration into catalog enrichment workflows at scale.

---

## 🛠️ Tech Stack

- 🧠 **FLAVA**: Multimodal embeddings
- 📦 **HDBSCAN**: Density-based clustering
- 🧾 **WordMap**: Frequency-based keyword summarization
- 🤖 **LLaMA-2**: LLM-based naming
- 📊 **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**: Data processing and visualization

---



