# Geneformer finetune

### Input files for TF dosage sensitivity classification task

*Update: original input files by the authors are [here](https://huggingface.co/ctheodoris/Geneformer/tree/main/examples/example_input_files).*

Input files for the [example notebook](https://huggingface.co/ctheodoris/Geneformer/blob/main/examples/gene_classification.ipynb) describing the finetuning process for transcription factor (TF) dosage sensitivity prediction.

| Input file                                                                                           |    Description    |   
| ----------------------------------------------------------------------------------------------------- | :------------------: | 
| [Dosage sensitivity TF labels](https://github.com/cx0/geneformer-finetune/blob/main/dosage_sens_tf/dosage_sens_tf_labels.csv)  | Dosage sensitivity predictions curated by Ni et al (2019) | 
| [Gene info table](https://github.com/cx0/geneformer-finetune/blob/main/dosage_sens_tf/gene_info_table.csv) | Ensemble gene IDs retrieved from Ensembl Genes 109 via BioMart | 


Ni et al (2019) gathered dosage sensitivity prediction scores from two sources:
- High confident haploinsufficient genes ([pLI>0.9](https://github.com/cx0/geneformer-finetune/blob/main/dosage_sens_tf/exac_lof_pLI_genes.txt)) from Lek et al (2016)
- Likely dosage sensitive genes ([HIPred>0.5](https://github.com/HAShihab/HIPred)) from Shihab et al (2017)

They also retrieved a set of all human transcription factors from Lampert et al (2018) ([human TF data v1.01](http://humantfs.ccbr.utoronto.ca/download.php)), and generated most reliable dosage-sensitive (MRDS) and dosage-insensitive (MRDIS) gene sets by considering support by each source dataset. Final list inclues 122 TFs with positive label (dosage sensitive, [MRDS](https://github.com/cx0/geneformer-finetune/blob/main/dosage_sens_tf/most_reliable_dosage_sensitive_TFs.csv)) and 368 TFs with negative label (dosage insensitive, [MRDIS](https://github.com/cx0/geneformer-finetune/blob/main/dosage_sens_tf/most_reliable_dosage_insensitive_TFs.csv)) out of a total of 1639 human TFs.




### References 
- Lambert, A. et al (2018) The human transcription factors. Cell 172 (4)
- Lek, M. et al (2016) Analysis of protein-coding genetic variation in 60,706 humans. Nature 536,
285–291
- Shihab, A. et al (2017) HIPred: an integrative approach to
predicting haploinsufficient genes. Bioinformatics 33, 1751–1757
- Ni, Z. et al (2019) Characterization of human dosage-sensitive
transcription factor genes. Front. Genet. 10, 1208