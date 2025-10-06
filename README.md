# Similarity-Analysis-of-SARS-CoV-2-Genomes-Using-IBSI

**Python | BioPython | Pandas | Matplotlib | Rank Correlation | Genomic Analysis**

A bioinformatics project that computes the **Information-Based Similarity Index (IBSI)** between **four SARS-CoV-2 chromosomes** from different countries using **k-mer distribution analysis** and **rank correlation (R²)**. The study quantifies genetic similarity and explores evolutionary relationships among viral strains, supporting genomic surveillance and vaccine development.

---

## 🧪 Project Overview

Since its emergence in **Wuhan, China (2019)**, the SARS-CoV-2 virus has caused a global pandemic, profoundly impacting public health and economies. Understanding its genomic structure is critical for tracking mutations, improving vaccines, and anticipating new variants.

This project applies **k-mer frequency analysis** and an **Information-Based Similarity Index (IBSI)** to measure how genetically similar four different SARS-CoV-2 genome sequences are. By analyzing the **rank correlation (R²)** of k-mer distributions (for k = 3 to 7), I provide a quantitative view of the relationships between viral strains from **China, Japan, Germany, and Bangladesh**.

---

## 📊 Objectives

* 🧬 Quantify genetic similarity among **four SARS-CoV-2 genomes**.
* 🔬 Use **k-mer distribution analysis (k=3 to 7)** to capture sequence-level variation.
* 📈 Compute **Information-Based Similarity Index (IBSI)** using **rank correlation (R²)**.
* 📊 Visualize pairwise genomic relationships with annotated 2D plots.
* 📑 Produce a similarity matrix for downstream phylogenetic or epidemiological studies.

---

## 🧬 Dataset Description

The project uses four complete SARS-CoV-2 genomes, each stored as a **FASTA** file:

| Accession ID  | Country    | Year | Description                     |
| ------------- | ---------- | ---- | ------------------------------- |
| **NC_045512** | China      | 2019 | Original Wuhan reference genome |
| **LC546038**  | Japan      | 2020 | Isolate from early outbreak     |
| **MT358643**  | Germany    | 2020 | European strain                 |
| **MT476385**  | Bangladesh | 2020 | South Asian strain              |

Each file contains the full genome sequence composed of the standard nucleotides **A, T, C, G**.

---

## 🧠 Methodology

| Step                     | Description                                                                    |
| ------------------------ | ------------------------------------------------------------------------------ |
| **1️⃣ Data Loading**     | Import FASTA sequences using **BioPython**, validating nucleotide composition. |
| **2️⃣ k-mer Generation** | Compute all possible **k-mers (3 ≤ k ≤ 7)** and their frequencies.             |
| **3️⃣ Ranking**          | Rank k-mers by frequency to create a comparable distribution between genomes.  |
| **4️⃣ IBSI Calculation** | Compute IBSI using **rank correlation (R²)** between pairs of genomes.         |
| **5️⃣ Visualization**    | Generate **annotated 2D scatter plots** showing rank relationships and R².     |
| **6️⃣ Results Analysis** | Summarize similarity scores and common k-mer counts in a results table.        |

---

## 📁 Project Structure

```
📂 SARS-CoV-2-IBSI
├── data/                         # FASTA genome files
├── notebooks/                    # Jupyter notebooks for analysis
├── src/                          # Main Python scripts
│   ├── ibsi_analysis.py
│   └── visualization.py
├── results/                      # R² results, plots, and similarity tables
├── README.md                     # Project documentation
└── requirements.txt              # Dependencies
```

---

## 🔍 Key Steps

1. **Data Preprocessing:** Validate and load genome sequences.
2. **K-mer Counting:** Generate and rank k-mer distributions for k = 3–7.
3. **IBSI Computation:** Calculate pairwise similarity (R²) for all genome combinations.
4. **Visualization:** Create rank correlation scatter plots with k-mer annotations.
5. **Reporting:** Summarize results into a CSV and a formatted similarity matrix.

---

## 🏆 Achievements & Results

* ✅ Successfully implemented IBSI computation across **6 genome pairs**.
* 📊 Identified high genetic similarity (R² > 0.98) between certain strains, indicating shared evolutionary origin.
* 📉 Detected subtle divergence (R² ≈ 0.94) in some pairs, reflecting mutation-driven evolution.
* 🧪 Produced **annotated rank plots** revealing conserved and variable genomic regions.
* 📁 Generated a comprehensive **IBSI similarity matrix** and exported results to CSV for further analysis.

---

## 📸 Visualizations

* 🧬 **2D Rank Scatter Plots:** Each plot shows k-mer rank relationships and IBSI (R²) between genome pairs.
* 📈 **IBSI Matrix Heatmap:** Visual summary of all pairwise similarity scores.
* 📊 **K-mer Distribution Graphs:** Frequency and diversity comparisons across genomes.

---

## 🧪 How to Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/SARS-CoV-2-IBSI.git
cd SARS-CoV-2-IBSI
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run the analysis

```bash
python src/ibsi_analysis.py
```

Or run interactively:

```bash
jupyter notebook notebooks/SARS_IBSI_Analysis.ipynb
```

---

## 🧭 Applications

* 🧬 **Viral Evolution Tracking** – Monitor mutation-driven genetic divergence.
* 💉 **Vaccine Development** – Identify conserved genome regions for target selection.
* 🦠 **Outbreak Surveillance** – Detect emerging variants and trace transmission.
* 🧫 **Comparative Genomics** – Study cross-strain similarities and lineage origins.

---

## 📚 Future Work

* 🔁 Extend analysis to >100 global SARS-CoV-2 strains.
* 🌍 Build phylogenetic trees directly from IBSI similarity data.
* 📊 Integrate mutation mapping and functional annotation.
