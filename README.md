# Drug repurposing of bromodomain inhibitors as a novel therapeutic for lymphatic filariasis guided by multi-species transcriptomics

Matthew Chung

2019-09-17

[![DOI](https://zenodo.org/badge/209141734.svg)](https://zenodo.org/badge/latestdoi/209141734)

The repository contains scripts and input_data_files to replicate the transcriptomics analysis in the manuscript. Additionally, the Supplementary Data for the manuscript is stored here.

## System requirements

R scripts were run using Windows 10 x64 with RStudio v1.1.447 using this R session:
```
R version 3.5.0 (2018-04-23)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows >= 8 x64 (build 9200)

Matrix products: default

locale:
[1] LC_COLLATE=English_United States.1252  LC_CTYPE=English_United States.1252    LC_MONETARY=English_United States.1252
[4] LC_NUMERIC=C                           LC_TIME=English_United States.1252    

attached base packages:
[1] grid      stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] ggdendro_0.1-20       pvclust_2.0-0         dendextend_1.9.0      factoextra_1.0.5      gridExtra_2.3         reshape_0.8.8        
 [7] ggplot2_3.1.0         gtools_3.8.1          WGCNA_1.66            fastcluster_1.1.25    dynamicTreeCut_1.63-1 edgeR_3.24.0         
[13] limma_3.38.2         

loaded via a namespace (and not attached):
 [1] matrixStats_0.54.0    robust_0.4-18         fit.models_0.5-14     bit64_0.9-7           doParallel_1.0.14     RColorBrewer_1.1-2   
 [7] rprojroot_1.3-2       prabclus_2.2-6        tools_3.5.0           backports_1.1.2       R6_2.3.0              rpart_4.1-13         
[13] Hmisc_4.1-1           DBI_1.0.0             lazyeval_0.2.1        BiocGenerics_0.28.0   colorspace_1.3-2      trimcluster_0.1-2.1  
[19] nnet_7.3-12           withr_2.1.2           tidyselect_0.2.5      bit_1.1-14            compiler_3.5.0        preprocessCore_1.44.0
[25] Biobase_2.42.0        htmlTable_1.12        labeling_0.3          diptest_0.75-7        scales_1.0.0          checkmate_1.8.5      
[31] DEoptimR_1.0-8        mvtnorm_1.0-8         robustbase_0.93-3     stringr_1.3.1         digest_0.6.18         foreign_0.8-70       
[37] rmarkdown_1.10        rrcov_1.4-4           base64enc_0.1-3       pkgconfig_2.0.2       htmltools_0.3.6       htmlwidgets_1.3      
[43] rlang_0.3.0.1         rstudioapi_0.8        RSQLite_2.1.1         impute_1.56.0         bindr_0.1.1           mclust_5.4.1         
[49] acepack_1.4.1         dplyr_0.7.6           magrittr_1.5          modeltools_0.2-22     GO.db_3.6.0           Formula_1.2-3        
[55] Matrix_1.2-14         Rcpp_1.0.0            munsell_0.5.0         S4Vectors_0.20.1      viridis_0.5.1         stringi_1.2.4        
[61] whisker_0.3-2         yaml_2.2.0            MASS_7.3-51.1         flexmix_2.3-14        plyr_1.8.4            blob_1.1.1           
[67] parallel_3.5.0        ggrepel_0.8.0         crayon_1.3.4          lattice_0.20-35       splines_3.5.0         locfit_1.5-9.1       
[73] knitr_1.20            pillar_1.3.0          fpc_2.1-11.1          codetools_0.2-15      stats4_3.5.0          glue_1.3.0           
[79] evaluate_0.12         latticeExtra_0.6-28   data.table_1.11.8     foreach_1.4.4         gtable_0.2.0          purrr_0.2.5          
[85] kernlab_0.9-27        assertthat_0.2.0      viridisLite_0.3.0     class_7.3-14          survival_2.41-3       pcaPP_1.9-73         
[91] tibble_1.4.2          iterators_1.0.10      AnnotationDbi_1.44.0  memoise_1.1.0         IRanges_2.16.0        bindrcpp_0.2.2
```

No non-standard hardware is required.

## Installation

RStudio installation is required along with the packages listed as follows:
```
 [1] ggdendro_0.1-20       pvclust_2.0-0         dendextend_1.9.0      factoextra_1.0.5      gridExtra_2.3         reshape_0.8.8
 [7] ggplot2_3.1.0         gtools_3.8.1          WGCNA_1.66            fastcluster_1.1.25    dynamicTreeCut_1.63-1 edgeR_3.24.0         
[13] limma_3.38.2        
```

Typical install time for RStudio and the listed packages should be <15 min

## Demo and Instructions for Use

Open Rmd scripts using RStudio and alter the input files to the files listed in the (3) input_data_files folder.    

## (1) scripts
The scripts folder contains three Rmd scripts used for the transcriptome analysis of each organism:

a) aaegypti_transcriptome_v2.Rmd

b) bmalayi_transcriptome_v2.Rmd

c) wbm_transcriptome_v2.Rmd

Each of the three scripts takes these inputs:

a) geneinfo - table containing functional annotation for the analyzed genes

b) counts - matrix of read counts for each gene, constructed as described in the Materials and Methods

c) tpm  - matrix of TPM for each gene

d) groups - used to assign groups and colors for the different samples

e) output directory path

Change the "Input file paths" code block to run the scripts on your local system.

## (2) htmls

Contains the output html files generated from the Rmd files in (1) scripts using the R package knitr. These are the expected outputs from each of the three scripts.

## (3) input_data_files

For each of the Rmd files, the inputs are:

### aaegypti_transcriptome.Rmd

```
geneinfo.path <- aaegypti_gene.info
counts.path <- aaegypti_counts.tsv
tpm.path <- aaegypti_tpm.tsv
groups.path <- aaegypti_groups.tsv
```

### bmalayi_transcriptome.Rmd

```
geneinfo.path <- bmalayi_gene.info
counts.path <- bmalayi_counts.tsv
tpm.path <- bmalayi_tpm.tsv
groups.path <- bmalayi_groups.tsv
```

### wbm_transcriptome.Rmd

```
geneinfo.path <- wbm_gene.info
counts.path <- wbm_counts.tsv
tpm.path <- wbm_tpm.tsv
groups.path <- wbm_groups.tsv
```

Each of these scripts should take <30 min.
