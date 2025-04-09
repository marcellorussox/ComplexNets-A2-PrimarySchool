# ComplexNets-A2-PrimarySchool

Welcome to the nerdiest corner of GitHub, where graph theory meets real-world chaos — a.k.a. face-to-face interactions among hyperactive primary school kids and their brave teachers.

## 📚 Project Overview
This repository contains the full analysis pipeline for investigating the **community structure** of a face-to-face interaction network collected in a French primary school, as described in the Sociopatterns project:

**[High-resolution measurements of face-to-face contact patterns in a primary school](http://www.sociopatterns.org/publications/high-resolution-measurements-of-face-to-face-contact-patterns-in-a-primary-school/)**

In this context:
- **Nodes** represent students or teachers.
- **Edges** indicate interactions, and **weights** denote total contact duration across two days.

The dataset is analyzed using **modularity maximization** algorithms to detect communities. We investigate both:
- The **unweighted network** (`primaryschool_u.net`)
- The **weighted network** (`primaryschool_w.net`)

Metadata on school groups is provided via `metadata_primary_school.txt`.

## 📃 Repository Structure
```
ComplexNets-A2-PrimarySchool/
├── ComplexNets-A2-PrimarySchool.ipynb   # The master notebook that does everything.
├── data/
│   ├── primaryschool_u.net              # Unweighted network
│   ├── primaryschool_w.net              # Weighted network
│   └── metadata_primary_school.txt      # Node attributes: school group membership
```

## 🧰 What You'll Find Inside

### ⚖️ Community Detection
We apply algorithms based on **modularity maximization** (e.g., Louvain) to:
- Discover meaningful groupings of individuals based on their interaction patterns.
- Compare the structures found in the **unweighted** vs **weighted** versions of the network.

### 📈 Visualization
- Node layout is computed using the **Kamada-Kawai** algorithm.
  - Important: We use **1/wij** as edge lengths in Kamada-Kawai.
  - But for community detection we stick to the **true weights**.
- Detected communities are color-coded.
- Node positions are fixed to those of the **weighted network** for consistent comparison.

### 🛋️ Community Composition by School Group
We analyze how each detected community maps to school group labels.
- Expect beautiful **stacked bar charts** and **pie charts** that show the overlap (or not) between structural and institutional groupings.

### 🧠 Interpretation
We include a concise but thoughtful discussion on:
- Structural differences between weighted and unweighted community detection results.
- Why **weights matter** — and when they reveal deeper social structures.

## ⚛️ How to Use
1. Clone the repo:
```bash
git clone https://github.com/YOUR_USERNAME/ComplexNets-A2-PrimarySchool.git
cd ComplexNets-A2-PrimarySchool
```
2. Open the notebook:
```bash
jupyter notebook ComplexNets-A2-PrimarySchool.ipynb
```
3. Run all cells and enjoy the graphs, plots, and social insight.

## 🚀 Bonus Nerd Points
- Full support for **weighted edge analysis** ✔️
- Metadata-aware community interpretation ✔️
- Nerd-grade plotting aesthetics ✔️
- Clean, modular notebook design ✔️

## 📖 Reference
Stehlé, J., et al. (2011). High-resolution measurements of face-to-face contact patterns in a primary school. *PloS one*, 6(8), e23176.

## 🛠️ License
MIT License. Go forth and modularize.

---

> "Communities are not found. They are *computed*."
