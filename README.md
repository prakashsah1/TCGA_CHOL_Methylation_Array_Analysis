# TCGA_CHOL_Methylation_Array_Analysis
This repository contains code and documentation for the analysis of DNA methylation in cholangiocarcinoma samples from the TCGA-CHOL study, using Illumina HumanMethylation450 BeadChip array data.

The goal of this project is to identify differentially methylated probes (DMPs), differentially methylated regions (DMRs), and their associated biological functions in tumor vs. normal tissue.

📋 Overview

Data source:
TCGA-CHOL (Cholangiocarcinoma) project, obtained from the Genomic Data Commons (GDC).
Platform:
Illumina HumanMethylation450 BeadChip array.
Key steps of the analysis:
Download and prepare methylation data using TCGAbiolinks.
Extract beta value matrix from the SummarizedExperiment object.
Perform quality control (QC) and visualize distributions (density plots, PCA).
Filter out problematic probes:
Probes with missing values (NA).
Probes on sex chromosomes (chrX, chrY).
Probes overlapping SNPs (MAF > 0.05).
Cross-reactive probes (Chen et al., 2013).
Convert beta values to M-values for statistical testing.
Identify DMPs using the limma package.
Identify DMRs using the DMRcate package.
Visualize DMRs using Gviz.
Perform gene ontology (GO) enrichment analysis with missMethyl.

🔗 References

Mishra, N. K., et al. (2020). Identification of Prognostic Markers in Cholangiocarcinoma Using Altered DNA Methylation and Gene Expression Profiles. Frontiers in Genetics, 11:522125. https://doi.org/10.3389/fgene.2020.522125
Maksimovic, J., Phipson, B., & Oshlack, A. (2016). A cross-package Bioconductor workflow for analysing methylation array data. F1000Research, 5:1281. https://doi.org/10.12688/f1000research.8839.2

📦 Packages Used

TCGAbiolinks
sesame
minfi
IlluminaHumanMethylation450kanno.ilmn12.hg19
limma
DMRcate
missMethyl
Gviz
GenomicRanges
RColorBrewer
