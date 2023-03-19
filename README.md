# INTRODUCTION
Bulk RNA sequencing allows to identify Differently Expressed genes (DE genes) across replicates in different conditions to functionally characterise them.
The data used for the analysis comes from Recount3, a public repository of RNA-seq experiments. Full unfiltered datasets for each of the three human tissues - brain, liver and lung- were retrieved.   



## QUALITY CONTROL
We removed samples with:
- a RIN (RNA integrity number) higher than 7
- the fraction of reads mapping on ribosomal RNA genes higher than 0.1 
- percentage of uniquely mapped reads lower than 85% 


## ANALYSIS 
Count table for the three tissues were built, genes were filtered by expression, removing altogether the ones with all or almost all 0 reads count. 
Normalisation - by TMM (Trimmed Mean of M-values) - was performed.

With the Multi Dimensional Scaling, we plot a projection of distance between gene expression profiles in 2 dimensions: what we want to assess is that replicates of the same tissue cluster well together.

To find the significant DE genes, a pairwise comparisons of gene expression between the three tissues was performed. Genes found to be overexpressed in one tissue against the other two were extracted, filtering and trimming the lists obtained by statistical significance:
- FDR < 0.01
- logCPM > 0
- excluding genes that have little or no annotation


## RESULTS
Significant genes for each tissue - overexpressed against the other two - were found..
The functional characterisation confirms that the DE analysis results are reliable. 


Analysis performd with @sabrisart

