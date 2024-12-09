# ecDNAscope

Extrachromosomal DNA (ecDNA) with abundant amplicons and high chromatin accessibility contributes significantly to tumor heterogeneity and an active transcriptome. We present ecDNAscope, a computational strategy designed to infer ecDNA structure and clonal trajectories from single-cell ATAC-seq data.EcDNAscope provides a robust tool for analyzing ecDNA structure, heterogeneity, and clonal trajectory.

---



The ecDNAscopeR package currently only supports Linux systems and requires a complex software environment. We strongly recommend users to run it within a conda environment.

### 1.creat conda environment

```bash
conda create -n  ecDNAscope python=3.7 r-base=4.3.2
conda activate ecDNAscope
```

### 2.Configure the software environment

```bash
# Install R packages
conda install -y bioconda::bioconductor-genomicranges # 1.54.1
conda install -y r-ggplot2=3.4.4
conda install -y r-seurat=4.3.0
conda install -y r-signac=1.14.0
conda install -y bioconda::bioconductor-chipseeker # 1.38.0
conda install -y bioconda::bioconductor-org.hs.eg.db # 3.18.0
conda install -y bioconda::bioconductor-txdb.hsapiens.ucsc.hg38.knowngene # 3.18.0
conda install -y bioconda::bioconductor-genesummary # 0.99.6
conda install -y bioconda::bioconductor-omiccircos # 1.40.0

# Install python packages
conda install -y numpy=1.19.5 pandas=1.3.5 scipy=1.7.3 statsmodels=0.13.2

# Install java8
conda install -y openjdk=8

# other packages
conda install -y samtools bedtools
```

### 3.Install ecDNAscope in R

```R
if(!require(devtools)) install.packages("devtools")
devtools::install_github("bigdata-lrkai/ecDNAscope")
```

