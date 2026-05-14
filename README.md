# AR Protein Visualization 🧬🥽
### Interactive Augmented Reality Tool for Molecular Protein Analysis — Microsoft HoloLens 2

Built during a summer research internship at **WINLAB, Rutgers University**, this project enables researchers to visualize and interact with 3D molecular protein structures in augmented reality using the Microsoft HoloLens 2. Proteins are pulled directly from the Rutgers Protein Data Bank, parsed into structured data, and rendered interactively in Unity.

---

## ✨ Features

- 🔬 **Live protein loading** — input any PDB code (e.g. `6PHQ`) to fetch and render the protein
- 🎨 **Full structural rendering** — Atoms, Bonds, Helices, Beta Sheets, and RNA all visualized
- 🖐️ **Hand & voice interaction** — manipulate proteins using HoloLens gestures and voice commands
- ⚡ **Optimized rendering** — mesh combining improved frame rate from **15 fps → 120 fps**
- 📱 **Mobile app** — camera-based interface for real-time interaction with scientific data

---

## 🔄 Pipeline

```
Input PDB Code (e.g. "6PHQ")
        │
        ▼
Rutgers Protein Data Bank
  ├── .pdb file
  └── .cif file
        │
        ▼
Python Web Scraper → Filtered CSV
        │
        ▼
Unity (C#) — Color atoms, build bonds, combine meshes
        │
        ▼
Microsoft HoloLens 2 — AR Rendering + Interaction
```

---

## 📊 Performance Optimization

A key challenge was rendering large proteins in real time on HoloLens 2 hardware. By combining meshes of similar objects and applying spline smoothing to curved structures:

| Metric | Before Optimization | After Optimization |
|---|---|---|
| CPU Frame Rate | 15 fps (66.7 ms) | 120 fps (8.3 ms) |
| GPU Frame Rate | — | 120 fps (8.3 ms) |

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Rendering Engine | Unity Game Engine |
| Scripting | C# |
| Data Pipeline | Python, NumPy |
| Data Source | Rutgers Protein Data Bank (RCSB PDB) |
| Hardware | Microsoft HoloLens 2 |
| Interaction | Hand gestures, voice commands |

---

## 🗂️ Supported Structural Features

- **Atoms** — color-coded by element type
- **Bonds** — rendered between bonded atom pairs
- **Helices** — smoothed using spline curves
- **Beta Sheets** — structural ribbon rendering
- **RNA** — base structure visualization

---

## 🚀 Getting Started

### Prerequisites
- Unity 2021.3+ with MRTK (Mixed Reality Toolkit)
- Microsoft HoloLens 2 (or HoloLens emulator)
- Python 3.9+ for the data pipeline

### Setup

```bash
git clone https://github.com/vir222/ar-protein-visualization.git
cd ar-protein-visualization

# Run the data pipeline to fetch a protein
cd pipeline
python fetch_protein.py --pdb_code 6PHQ
```

Then open the Unity project, load the generated CSV, and deploy to HoloLens 2 via Visual Studio.

---

## 👥 Team

| Name | School |
|---|---|
| Vir Vaidya | Rutgers University — Computer Engineering |
| Samhitha Sangaraju | Rutgers University — Computer Science & Data Science |
| Alexander Kim | Ohio State University — Computer Science |

**Supported by:** WINLAB @ Rutgers, RCSB PDB team, Ivan Seskar, Jennifer Shane, Prof. Wade Trappe, Prof. Ashley Guo

---

## 👤 Contact

**Vir Vaidya** — vv275@rutgers.edu  
Summer Research Internship, WINLAB, Rutgers University — 2024
