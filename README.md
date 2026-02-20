CNV_Methylation_Analysis
End-to-end reproducible R pipeline for integrative DNA methylation and copy number variation (CNV) analysis in High-Grade Serous Ovarian Cancer (HGSOC).
Datasets
GSE81224 (10 Normal + 10 Untreated samples)
GSE65820 (121 Treated samples)
Total Samples: 141
Raw IDAT files were obtained from the NCBI GEO database.
⚠️ Note: GEO raw files (IDATs) are not included in this repository due to GitHub file size constraints. Users can download the datasets directly from GEO using the accession numbers above.
Workflow Overview
1. DNA Methylation Processing
•	IDAT import using minfiQuantile normalization
•	Beta value extraction
•	Differential methylation analysis using limma
•	Top 200 CpG identification per comparison
•	CpG annotation (Illumina EPIC)
2. Comparative Analysis
•	Treated vs Normal
•	Untreated vs Normal
•	Extraction of top 100 gene-associated CpGs
•	Venn analysis to identify common genes
3. Transcription Factor Mapping
•	TF-target association using TRRUST database
•	Identification of regulatory interactions among common genes
4. Targeted CpG Methylation Assessment
•	Beta-value based methylation status classification
•	Site-specific methylation evaluation
5. CNV Profiling
•	CNV segmentation extraction
•	Amplification/deletion classification
•	Chromosome-wise CNV distribution analysis
•	Whole-genome CNV visualization
•	Automated CSV export for reproducibility
Output Files
•	Annotated DMR tables
•	Gene lists
•	Common gene intersection
•	TRRUST TF mapping results
•	CNV segmentation summaries
•	Chromosome-level CNV distribution plots

Reproducibility
All scripts are written in R and structured for full reproducibility provided that raw GEO data is downloaded and directory paths are updated accordingly.
