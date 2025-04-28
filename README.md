Investigating Mobile Genetic Elements as Vectors of Antimicrobial Resistance in _Klebsiella pneumoniae_ Using Machine Learning Techniques

Overview

This repository contains all scripts and supplementary material for the MSci research project:
“Investigating Mobile Genetic Elements (MGEs) as Vectors for Antimicrobial Resistance (AMR) in _Klebsiella pneumoniae_ Using Machine Learning Techniques.”

The project combines genomic analysis, mobile element detection, and interpretable machine learning models to predict resistance phenotypes and investigate the role of plasmids and bacteriophages in AMR in _Klebsiella pneumoniae_.

Repository Structure
•	Docs/: Project report, supplementary data, and figures.
•	Scripts/: Stepwise Python scripts and shell scripts used throughout the workflow, clearly named (e.g., Step 01, Step 02, etc.)

Each script is numbered according to the order used in the pipeline, making it easy to follow and replicate the analysis.

Summarised Methodological Workflow
(detailed to a greater extent in report)
1.	Genome Collection
Downloaded 1,057 K. pneumoniae genomes from BVBRC, filtered by antibiotic susceptibility data.
2.	Mobile Element Detection
•	MGEs identified using geNomad.
•	Prophage regions masked to prevent bias in ARG detection.
3.	Resistance Gene Identification
•	RGI (CARD database) for ARG annotation.
•	Cross-validated with StarAMR and AMRFinderPlus.
4.	Pangenome Analysis
•	Functional annotation (Prokka).
•	Pangenome construction (Roary).
•	Phylogenetic tree building (FastTree).
5.	Co-Association Analysis
•	Coinfinder to detect significant gene co-associations.
6.	Machine Learning
•	Binary phenotype labelling.
•	Decision tree classifiers (Weka J48) for predicting resistance to ciprofloxacin, gentamicin, and meropenem.
7.	Data Interpretation
•	Linking plasmid vs. chromosomal origin of genes.
•	Investigating co-dependencies between MGEs and chromosomal genes in resistance expression.

How to Reproduce

Each major step corresponds to a folder or script:
•	Navigate to Scripts/
•	Follow the scripts sequentially from Step 01 onwards.
•	Dependencies include: Python 3, Sourmash, geNomad, RGI, Roary, Coinfinder, FastTree, Weka.

(Exact versions used are noted in the full report.)

Key Findings
•	Plasmids significantly contribute to resistance but often require chromosomal co-association.
•	Prophage contribution to AMR in K. pneumoniae appears limited compared to plasmids.
•	Machine learning models revealed both known and novel gene predictors of resistance.

Citation

If you use any part of this repository, please cite:
C. Woods, E. T. Campbell, L. Dillon, C. Creevey  (2025). Investigating Mobile Genetic Elements as Vectors for Antimicrobial Resistance in Klebsiella pneumoniae Using Machine Learning Techniques. MSci Dissertation – Queen’s University Belfast

