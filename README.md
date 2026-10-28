# Docking and Molecular Dynamics of the Natural Diterpenoid Dihydrotanshinone I in Human 15-PGDH Across Three Inhibitor-Bound Receptor Structures

**Author(s):** [Sabbir Ahmad Antor](https://orcid.org/0009-0008-4020-2316), [Md Abu Sadat Soash](https://orcid.org/0009-0001-1116-2449), Muktadir Al Mahmud, [Raphael Kabir Niloy](https://orcid.org/0009-0006-4907-4221), [Md. Mainul Hossain Bakul](https://orcid.org/0009-0003-2929-6271), [Gokul Chandra Biswas](https://orcid.org/0000-0001-9097-6426)  
**Academic Supervisor:** [Prof. Dr. Gokul Chandra Biswas](https://www.sust.edu/departments/geb/faculty/gcbiswas-geb@sust.edu)  
*Department of Genetic Engineering and Biotechnology*<br>
*Shahjalal University of Science and Technology, Sylhet, Bangladesh*

[![Preprint: Research Square](https://img.shields.io/badge/Preprint-10.21203%2Frs.3.rs--10719902%2Fv1-blue.svg?style=flat-square)](https://doi.org/10.21203/rs.3.rs-10719902/v1)
[![Dataset: Zenodo](https://img.shields.io/badge/Zenodo-10.5281%2Fzenodo.21945974-success.svg?style=flat-square)](https://doi.org/10.5281/zenodo.21945974)
[![Target: Human%2015--PGDH](https://img.shields.io/badge/Target-Human%2015--PGDH-red.svg?style=flat-square)](https://www.rcsb.org/structure/9PFL)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg?style=flat-square)](https://creativecommons.org/licenses/by/4.0/)

---

## Abstract

15-hydroxyprostaglandin dehydrogenase (15-PGDH) is the committed NAD(+)-dependent oxidoreductase that catabolizes prostaglandin E2 (PGE2) into its biologically inactive 15-keto form. Sarcopenia, the progressive loss of skeletal muscle mass and functional strength during aging, is directly exacerbated by diminished PGE2 signaling. Pharmacological or genetic inhibition of 15-PGDH elevates endogenous PGE2 levels and restores mitochondrial function and muscle regenerative capacity. While synthetic inhibitors have advanced to preclinical maturity, structurally characterized botanical inhibitors remain scarce, and the lipophilic phenanthraquinones of *Salvia miltiorrhiza* (Danshen) have remained uncharacterized against 15-PGDH.

In this study, the natural abietane diterpenoid **dihydrotanshinone I** (alongside panaxynol as a mechanistically distinct natural comparator) was docked across an ensemble of three experimentally determined human 15-PGDH receptor conformations: the high-resolution X-ray co-crystals **9PFL** (1.65 Angstrom) and **9PFM** (1.88 Angstrom), and the lid-closed Cryo-EM structure **8CVN** (2.40 Angstrom). The docking protocol was validated by crystallographic self-redocking, which reproduced native binding modes within heavy-atom RMSDs of 0.38 to 1.46 Angstrom. Dihydrotanshinone I docked favorably into the active site pocket across all three structures with predicted binding affinities ranging from $-8.94\text{ to }-10.5\text{ kcal/mol}$, engaging catalytic triad residues (Ser138, Tyr151) and the structural lid hinges (Phe185, Tyr217). Across fifteen independent random seeds per receptor, top poses converged within $0.10\text{ to }0.18\text{ Angstrom}$ RMSD, demonstrating that docking solutions were independent of stochastic seed artifacts.

To assess the dynamic persistence of the docked complexes, **triplicate 100 ns explicit-solvent molecular dynamics (MD) simulations** were executed for each system (9 trajectories; 900 ns cumulative sampling). Dihydrotanshinone I remained continuously bound to the inhibitor pocket throughout all nine trajectories, maintaining persistent contact with lid-hinge residue Phe185 ($94.6\%\text{ to }100\%$ occupancy), while Lys155 showed exactly zero contact, corroborating its role in cofactor coordination rather than inhibitor binding. These combined in silico findings identify dihydrotanshinone I as a reproducible, mechanistically plausible natural-compound candidate for the 15-PGDH inhibitor pocket.

---

## 1. Biological Background & Pharmacological Context

```
                          Aging & Sarcopenia Cascade
                                       |
                                       v
               Downregulated Prostaglandin E2 (PGE2) Signaling
                                       |
                   [Muscle Stem Cell Regeneration Failure]
                                       |
                                       v
      +-----------------------------------------------------------------+
      | Committed Catabolic Degradation:                                |
      | PGE2  ---( 15-PGDH / NAD+ )--->  15-keto-PGE2 (Inactive)        |
      +-----------------------------------------------------------------+
                                       |
               Target Strategy: Inhibit 15-PGDH Oxidoreductase
                                       |
                                       v
                     Elevation of Endogenous Muscle PGE2
                                       |
                     Rejuvenation of Aged Skeletal Muscle
```

### 1.1 Sarcopenia and the 15-PGDH Therapeutic Node
Loss of skeletal muscle mass and contractile strength during aging severely undermines physiological independence. The eicosanoid mediator **prostaglandin E2 (PGE2)** regulates muscle stem cell proliferation and regenerative myogenesis. Intracellular PGE2 bioavailability is regulated by 15-hydroxyprostaglandin dehydrogenase (15-PGDH), a homodimeric oxidoreductase that oxidizes the 15-hydroxyl group of PGE2. Genetic ablation or small-molecule inhibition of 15-PGDH (e.g., SW033291) elevates localized PGE2, rejuvenating aged muscle mass, grip strength, and mitochondrial respiration (*Palla et al., Science, 2021*).

### 1.2 Dihydrotanshinone I: A Rigid Natural Bioactive Scaffold
Dihydrotanshinone I is a principal lipophilic phenanthraquinone from *Salvia miltiorrhiza* (Danshen), an established medicinal plant. Its rigid abietane diterpenoid core, low rotatable-bond count, and documented modulation of inflammatory signaling make it an attractive candidate for targeting the orthosteric pocket of 15-PGDH.

```
Compound Summary:
- Molecule: Dihydrotanshinone I
- PubChem CID: 11425923
- Chemical Formula: C18 H14 O3
- Molecular Weight: 278.3 g/mol
- Structural Class: Abietane Diterpenoid Phenanthraquinone
- Natural Source: Salvia miltiorrhiza (Danshen)
```

---

## 2. Experimental Ensemble & In Silico Pipeline

```
+---------------------------------------------------------------------------------+
| 1. Experimental 15-PGDH Receptor Preparation                                    |
|    - 9PFL (X-ray, 1.65 A, NAD-bound)                                            |
|    - 9PFM (X-ray, 1.88 A, NAD-bound)                                            |
|    - 8CVN (Cryo-EM, 2.40 A, NADH-bound, lid-closed conformation)                 |
+---------------------------------------------------------------------------------+
                                         |
                                         v
+---------------------------------------------------------------------------------+
| 2. Protocol Validation via Self-Redocking                                       |
|    - Extract crystallographic native inhibitors and redock into cognate pockets |
|    - Validation Benchmark: RMSD <= 2.0 A (Observed: 0.38 A, 0.56 A, 1.46 A)    |
+---------------------------------------------------------------------------------+
                                         |
                                         v
+---------------------------------------------------------------------------------+
| 3. High-Exhaustiveness Molecular Docking                                         |
|    - AutoDock Vina 1.2.7 (Exhaustiveness = 32, Grid Cube = 24 A)                |
|    - Multi-scoring rescoring (Vina vs. Vinardo)                                 |
|    - Stochastic seed-robustness audit across 15 independent random seeds        |
+---------------------------------------------------------------------------------+
                                         |
                                         v
+---------------------------------------------------------------------------------+
| 4. Explicit-Solvent Molecular Dynamics Simulations                              |
|    - Engine: GROMACS 2026.3 | Force Field: AMBER ff14SB + GAFF2 (AM1-BCC)       |
|    - Replicates: Triplicate 100 ns trajectories per system (9 runs = 900 ns)    |
|    - Analyses: Ligand RMSD, per-residue contact occupancy, H-bond geometry     |
+---------------------------------------------------------------------------------+
```

---

## 3. Key Findings and Quantitative Benchmark

### 3.1 Crystallographic Redocking Validation

Self-redocking of co-crystallized inhibitors reproduced native poses within strict sub-2 Angstrom tolerances, confirming search space parameters and scoring accuracy across both X-ray and Cryo-EM models:

| Structure | Method | Resolution | Bound Cofactor | Redocked Native Inhibitor | Redock Affinity | Heavy-Atom RMSD | Validation Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **9PFL** | X-ray | $1.65\text{ \AA}$ | $\text{NAD}^+$ | A1CH2 | $-13.61\text{ kcal/mol}$ | **$0.379\text{ \AA}$** | **Pass** |
| **9PFM** | X-ray | $1.88\text{ \AA}$ | $\text{NAD}^+$ | SWL | $-8.85\text{ kcal/mol}$ | **$0.564\text{ \AA}$** | **Pass** |
| **8CVN** | Cryo-EM | $2.40\text{ \AA}$ | $\text{NADH}$ | SWL / SW209415 | $-8.82\text{ kcal/mol}$ | **$1.462\text{ \AA}$** | **Pass** |

### 3.2 Predicted Docking Affinities & Contact Fingerprints

* Dihydrotanshinone I attained docking scores of $-8.94\text{ kcal/mol}$ in 9PFL, $-9.56\text{ kcal/mol}$ in 9PFM, and $-10.50\text{ kcal/mol}$ in 8CVN.
* In X-ray models, the compound forms a direct hydrogen bond with catalytic residue **Ser138** ($2.89\text{ \AA}$ in 9PFL, $2.83\text{ \AA}$ in 9PFM) and contacts **Tyr151** and lid hinge **Phe185**.
* In Cryo-EM structure 8CVN, it anchors tightly on the dual lid-hinge residues **Phe185** ($3.16\text{ \AA}$) and **Tyr217** ($3.52\text{ \AA}$).
* **Seed Convergence**: Testing 15 independent random seeds demonstrated complete convergence (15 of 15 seeds in the dominant cluster) with pairwise RMSDs $\le 0.18\text{ \AA}$.

### 3.3 Molecular Dynamics (9 x 100 ns Trajectories)

All nine 100 ns trajectories completed without structural disintegration or ligand dissociation:
* **Continuous Pocket Occupancy**: Minimum protein-ligand heavy-atom distance never exceeded $4.5\text{ \AA}$ in any frame across 90,027 analyzed frames.
* **Persistent Anchor**: Lid hinge **Phe185 remained in contact for $94.6\%\text{ to }100\%$ of frames** across all systems and replicas, behaving as a rigid, essential hydrophobic anchor.
* **Cofactor Integrity**: **Lys155 maintained 0.0% contact occupancy** with the ligand across all nine runs, validating that the ligand does not displace the catalytic cofactor coordination network.
* **Lid Mobility Partitioning**: Per-residue RMSF demonstrated that Phe185 remains structurally rigid (lower than protein average RMSF), whereas Tyr217 accounts for the flexible breathing motion of the induced-fit lid.

---

## 4. Repository Structure

```
dihydrotanshinone-15pgdh-dynamics/
|-- .gitignore                                    # Simulation binary and temporary file exclusions
|-- README.md                                     # Full technical and methodological documentation
`-- MD of Natural Diterpenoid Dihydrotanshinone I.pdf  # Complete published preprint manuscript
```

---

## 5. Data and Reproducibility Archive

All computational assets, coordinate files, force field parameters, and simulation runs are permanently archived on Zenodo in accordance with open-science standards:

* **Zenodo Repository**: [10.5281/zenodo.21945974](https://doi.org/10.5281/zenodo.21945974)
* **Archived Components**:
  * PDBQT receptor coordinates for 9PFL, 9PFM, and 8CVN with reconstructed NAD(+)/NADH cofactors.
  * Meeko-parameterized ligand topologies for dihydrotanshinone I and panaxynol.
  * AutoDock Vina search configurations and 15-seed convergence outputs.
  * AMBER ff14SB / GAFF2 GROMACS topologies (`.top`, `.gro`) and run-input parameters (`.mdp`).
  * 9 individual production MD trajectories (100 ns each).

---

## 6. Citation & Scholarly Reference

If you utilize this methodology, docking protocols, or parameter files in your research, please cite the published preprint:

```bibtex
@article{antor2026docking,
  title={Docking and Molecular Dynamics of the Natural Diterpenoid Dihydrotanshinone I in Human 15-PGDH Across Three Inhibitor-Bound Receptor Structures},
  author={Antor, Sabbir Ahmad and Soash, Md Abu Sadat and Mahmud, Muktadir Al and Niloy, Raphael Kabir and Bakul, Md. Mainul Hossain and Biswas, Gokul Chandra},
  journal={Research Square},
  year={2026},
  doi={10.21203/rs.3.rs-10719902/v1},
  url={https://doi.org/10.21203/rs.3.rs-10719902/v1}
}
```

---

## 7. Authorship & Correspondence

* **Authors**: Sabbir Ahmad Antor, Md Abu Sadat Soash, Muktadir Al Mahmud, Raphael Kabir Niloy, Md. Mainul Hossain Bakul, Gokul Chandra Biswas
* **Research Supervision**: [Prof. Dr. Gokul Chandra Biswas](https://www.sust.edu/departments/geb/faculty/gcbiswas-geb@sust.edu)
* **Affiliation**: Department of Genetic Engineering and Biotechnology, Shahjalal University of Science and Technology, Sylhet, Bangladesh
* **License**: Creative Commons Attribution 4.0 International ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/))
