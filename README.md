# Comparative Transcriptomics: Basal-like vs. Luminal Breast Cancer
**Subtype-specific Biomarker Discovery using RNA-Seq Data (GSE52194)**

##  Project Overview
This project identifies the molecular signatures distinguishing aggressive Basal-like (Triple-Negative) breast cancer from Luminal subtypes. By utilizing a standardized bioinformatics pipeline, we identified **972 high-confidence Differentially Expressed Genes (DEGs)**, highlighting novel therapeutic targets and metabolic vulnerabilities in the Basal phenotype.

##  Bioinformatics Pipeline (Galaxy)
This analysis was conducted within the **Galaxy Project** ecosystem to ensure full computational reproducibility.

1. **Quality Control:** `FastQC` v0.74 (Validated base quality Phred > 30).
2. **Read Alignment:** `HISAT2` v2.2.1 (Mapped to Human Reference Genome hg38).
3. **Quantification:** `featureCounts` v2.0.3 (Gene-level read summarization).
4. **Differential Expression:** `DESeq2` v1.34.0 (Thresholds: $P_{adj} < 0.05$ and $|Log_2FC| \ge 1.0$).
5. **Pathway Analysis:** `goseq` and `Pathview` (KEGG pathway enrichment and visualization).

##  Repository Contents
* **`Final_Project_Report.pdf`**: Comprehensive research report including methodology, results, and discussion.
* **`Transcriptomics_Workflow.ga`**: The complete Galaxy workflow file. (Import this into Galaxy to reproduce the entire pipeline).
* **`Supplementary_Data_1_DEGs.xlsx`**: The full list of 972 differentially expressed genes with statistical values.

##  Key Findings
* **Primary Basal Markers:** Identified significant upregulation of $KRT16$, $PTCHD1$, and $FOLH1$.
* **Primary Luminal Markers:** Significant expression of $TFF1$ and $ERBB4$.
* **Clinical Implications:** Discovered activation of the $CACNA1B$ calcium signaling axis as a potential druggable vulnerability in Basal-like tumors.

## 🔗 Data Source
Raw sequencing data (FASTQ) was retrieved from the **NCBI Gene Expression Omnibus (GEO)** under accession [GSE52194](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE52194).

---
**License:** MIT
