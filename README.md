# LMX1A_iPSC_DA
A repository of RMarkdown files used to analyze sc-RNA sequencing data from induced Pluripotent Stem Cell derived dopaminergic neurons of the LMX1A Cre AAVS1 BFP line.

## Data availability

Raw and processed gene expression data has been deposited in GEO:
+ Time Course experiment [GSE247600](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE247600)..

### Time course

+ Metadata: [GSE247600_TimeCourse_metadata.tsv.gz](https://ftp.ncbi.nlm.nih.gov/geo/series/GSE247nnn/GSE247600/suppl/GSE247600%5FTimeCourse%5Fmetadata.tsv.gz)
  
+ Count data per sample

  [GSM7897844_HET1D21_S2_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897844/suppl/GSM7897844%5FHET1D21%5FS2%5Fgenematrix.csv.gz)
  
  [GSM7897845_HET2D21_S1_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897845/suppl/GSM7897845%5FHET2D21%5FS1%5Fgenematrix.csv.gz)

  [GSM7897846_HET1D30_S5_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897846/suppl/GSM7897846%5FHET1D30%5FS5%5Fgenematrix.csv.gz)

  [GSM7897847_HET2D30_S6_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897847/suppl/GSM7897847%5FHET2D30%5FS6%5Fgenematrix.csv.gz)

  [GSM7897849_HET1D45WHOLE_S7_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897849/suppl/GSM7897849%5FHET1D45WHOLE%5FS7%5Fgenematrix.csv.gz)

  [GSM7897850_HET1D65_S9_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897850/suppl/GSM7897850%5FHET1D65%5FS9%5Fgenematrix.csv.gz)

  [GSM7897851_HET2D65_S10_genematrix.csv.gz](https://ftp.ncbi.nlm.nih.gov/geo/samples/GSM7897nnn/GSM7897851/suppl/GSM7897851%5FHET2D65%5FS10%5Fgenematrix.csv.gz)
  
+ Normalized data: [GSE247600_TimeCourse_normalized_data.tsv.gz](https://ftp.ncbi.nlm.nih.gov/geo/series/GSE247nnn/GSE247600/suppl/GSE247600%5FTimeCourse%5Fnormalized%5Fdata.tsv.gz)

External data used as reference to annotate clusters (human embryonic midbrain / hEM)
+ Data obtained from GEO [GSE76381](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE76381).

# To start
Download gene expression data and metadata.

# RMarkdown scripts

+ *00_TimeCourse_DataFiltering_DEA.Rmd*
  Time course data filtering, normalization, scaling, clustering, annotation using the hEM as reference, PCA, UMAP, differential expression analysis per time point and per clone.
+ *01_TimeCourse_Velocity_Pseudotime.Rmd*
  RNA velocity analysis and projection into UMAP. Please note you will need to download the genematrix files including introns (<SAMPLE>_incl_introns_genematrix.csv.gz) from GEO.
+ *02_Sorted_MPP_DataFiltering_DEA.Rmd*
  Non Sorted (NS), and sorted (BFP+ and BFP-) data filtering, normalization, scaling, clustering, annotation of MPP+ treated data based on the basal condition, PCA, UMAP and differential expression analysis per cluster and per sorted type.
+ *03_Sorted_MPP_vs_Basal_B3.Rmd*
  Differential expression analysis on the B3 basal and B3 predicted MPP+ treated cells.  

# License
Distributed under the MIT License. See License.txt for more information.
