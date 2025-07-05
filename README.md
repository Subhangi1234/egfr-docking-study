# 🧬 EGFR Docking Study

### Molecular Docking of FDA-Approved Cancer Drugs with EGFR Tyrosine Kinase Domain (PDB ID: 1M17)

---

## 📌 Overview

This project investigates the **binding efficiency of three FDA-approved cancer drugs** — Erlotinib, Gefitinib, and Imatinib — against the **EGFR tyrosine kinase domain** using molecular docking techniques. The protein structure used for docking is **PDB ID: 1M17**, representing EGFR in complex with a known inhibitor (Erlotinib).

The goal is to compare the **binding affinities**, identify **key molecular interactions**, and interpret the potential of **cross-target binding** using computational tools.

---

## 🧪 Tools & Databases Used

- **Protein Structure**: RCSB PDB (PDB ID: 1M17)  
- **Ligand Structures**: PubChem  
- **Molecular Docking**: PyRx (AutoDock Vina)  
- **File Conversion & Energy Minimization**: Open Babel (via PyRx)  
- **Visualization & Analysis**: Discovery Studio Visualizer  
- **Data Organization**: Microsoft Excel

---

## 🔬 Methodology

### 1. **Protein Preparation**
- Downloaded EGFR crystal structure (PDB: 1M17)
- Cleaned the structure in Discovery Studio:
  - Removed water molecules and co-crystallized ligand (Erlotinib)
  - Added hydrogen atoms
- Saved as `clean_egfr.pdb`

### 2. **Ligand Preparation**
- Selected 3 FDA-approved drugs:
  - ✅ Erlotinib *(EGFR inhibitor)*
  - ✅ Gefitinib *(EGFR inhibitor)*
  - ✅ Imatinib *(non-EGFR kinase inhibitor)*
- Downloaded `.sdf` files from PubChem
- Converted to `.pdb` using Discovery Studio
- Performed **energy minimization** in PyRx (Open Babel)
- Converted to `.pdbqt` for docking

### 3. **Molecular Docking**
- Imported protein and ligands into PyRx
- Defined the macromolecule: `clean_egfr.pdb`
- Set the docking grid around the known active site (Erlotinib binding pocket)
- Used **AutoDock Vina** to dock each ligand
- Exported binding affinities to Excel

### 4. **Interaction Analysis**
- Chose **Model 1** from Vina output (best pose)
- Visualized ligand-protein complexes in Discovery Studio
- Merged ligand with receptor and defined ligand
- Generated:
  - 3D binding poses
  - Surface representations
  - 2D interaction diagrams (H-bonds, π-π stacking, hydrophobic contacts)

---

## 📊 Docking Results

| Ligand     | Binding Affinity (kcal/mol) | Interpretation        |
|------------|------------------------------|------------------------|
| **Imatinib**  | **–10.2** ✅               | Strongest binder       |
| Gefitinib  | –7.8                         | Moderate binder        |
| Erlotinib  | –6.9                         | Weakest binder         |

---

## 🧠 Key Insight

> Although **Imatinib** is not an EGFR-specific drug, it showed the **strongest binding affinity** (–10.2 kcal/mol) with EGFR in this study. This suggests potential **cross-reactivity** or **structural mimicry** in the kinase binding domain, highlighting possible implications in **drug repurposing** and the design of multi-target inhibitors.

---

## 🔍 Ligand-Protein Interaction Summary

| Ligand     | H-Bonds | π-π Stacking | Hydrophobic Contacts | Notes             |
|------------|---------|--------------|-----------------------|-------------------|
| Imatinib   | 3       | 1            | 5                     | Best binder       |
| Gefitinib  | 2       | 1            | 4                     | EGFR-specific     |
| Erlotinib  | 1       | 1            | 3                     | EGFR-specific     |

---

## 🖼 Visualizations

### 🧪 Imatinib–EGFR Complex
**3D Binding Pose**
![Imatinib 3D](./visuals/imatinib_3d.png)

**2D Interaction Diagram**
![Imatinib 2D](./visuals/imatinib_2d.png)

---

### 🧪 Gefitinib–EGFR Complex
**3D Binding Pose**
![Gefitinib 3D](./visuals/gefitinib_3d.png)

**2D Interaction Diagram**
![Gefitinib 2D](./visuals/gefitinib_2d.png)

---

### 🧪 Erlotinib–EGFR Complex
**3D Binding Pose**
![Erlotinib 3D](./visuals/erlotinib_3d.png)

**2D Interaction Diagram**
![Erlotinib 2D](./visuals/erlotinib_2d.png)

---

## 📁 Project Structure

```
egfr-docking-study/
│
├── protein/
│ └── clean_egfr.pdb
├── ligands/
│ ├── erlotinib.pdb
│ ├── gefitinib.pdb
│ └── imatinib.pdb
├── docking_results/
│ ├── *.pdbqt files
│ └── docking_scores.xlsx
├── visuals/
│ └── *.png screenshots
└── README.md

yaml
Copy
Edit
```

---

## 📌 Author

**Subhangi Majumder**  
B.Tech Biotechnology  
Molecular Docking & Bioinformatics Enthusiast  

---

## ✅ Status
- [x] Protein and ligand preparation
- [x] Docking with AutoDock Vina
- [x] Visualization and interaction analysis
- [x] Project documentation and result interpretation
- [ ] Future prospect: Adding more ligands for extended analysis  

---

## ⭐ How to Cite or Use This Work

This project is intended for academic, training, and demonstration purposes. Please feel free to fork, cite, or build upon it with appropriate credit.

