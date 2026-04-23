# ovarian-cancer-genomic-analysis
# Structural and Genomic Analysis of Chemotherapy Resistance in High-Grade Serous Ovarian Cancer (HGSOC)

![Bioinformatics](https://img.shields.io/badge/Bioinformatics-Dry_Lab-blue)
![Structural Biology](https://img.shields.io/badge/Structural_Biology-Wet_Lab_Focus-green)
![GATK](https://img.shields.io/badge/Pipeline-GATK-orange)

## 📌 Project Overview
This project investigates the genomic mechanisms underlying chemotherapy resistance in Ovarian Cancer, with a specific focus on **TP53** and **BRCA1** mutations. By bridging dry-lab variant calling pipelines with wet-lab structural biology principles, this study models how specific point mutations disrupt protein-DNA interactions and drive clinical drug resistance.

## 🔬 Bioinformatics Pipeline (Dry-Lab)
The genomic data was processed using a standard targeted Whole Exome Sequencing (WES) pipeline to identify critical somatic variants.
* **Alignment & Pre-processing:** BWA-MEM mapping to the hg38 reference genome, followed by sorting and indexing.
* **Variant Calling:** GATK HaplotypeCaller was utilized to generate the raw mutation profiles.
* **Output:** The resulting `.vcf` (Variant Call Format) file successfully isolated the clinically significant variations from the raw reads.

## 🧬 Structural Consequence & Clinical Interpretation (Wet-Lab Perspective)
Finding the mutation in a text file is only half the battle. To understand the *mechanism* of resistance, the identified **TP53 (R175H)** mutation was modeled *in silico* using **ChimeraX**. 

The R175H mutation replaces a positively charged Arginine with a Histidine in the DNA-binding domain of the p53 tumor suppressor protein. This structural alteration disrupts the zinc-binding pocket, preventing p53 from anchoring to DNA and inducing apoptosis in response to chemotherapy-induced DNA damage.

### Structural Comparison
*(Below is the visualization of the mutation site)*

**1. Wild-Type TP53 (Healthy DNA Binding)**
<img width="2500" height="1499" alt="p53_DNA_final" src="https://github.com/user-attachments/assets/d448f72a-0515-49ab-b1c0-46a346e5736e" />

*Visualization of the wild-type Arginine-175 (Red) properly structurally supporting the DNA-binding domain.*

**2. Mutant TP53 - R175H (Loss of Function)**
<img width="2500" height="1499" alt="p53_DNA_mutant_R175H" src="https://github.com/user-attachments/assets/b502d266-b2a6-43af-972a-8dd07d84a52a" />

*In silico mutagenesis demonstrating the structural distortion caused by the Histidine substitution (Magenta), leading to impaired DNA interaction.*

## 📂 Repository Structure
* `Ovarian_Cancer_Targeted_WES.ipynb`: The complete Jupyter Notebook containing the bash scripts, GATK commands, and pipeline documentation.
* `ovarian_cancer_variants.vcf`: The raw variant call output containing the identified genomic alterations.
* `/images`: Directory containing the high-resolution ChimeraX 3D molecular models.

## 🎯 Conclusion
This workflow demonstrates a comprehensive approach to modern oncology research: starting from raw sequencing reads, executing a standardized bioinformatics pipeline, and concluding with a structural biology interpretation of the clinical phenotype.
