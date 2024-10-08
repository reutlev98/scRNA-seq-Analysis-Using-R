
# scRNA-seq Analysis of Lung Cells from Adult Mouse

## Overview
This project focuses on the analysis of single-cell RNA sequencing (scRNA-seq) data of lung cells isolated from an adult mouse, using data provided by 10X Genomics. The primary objective was to identify cell types by analyzing gene expression patterns, clustering the cells, and comparing the clusters with known reference data.

## Project Objectives
- Perform an analysis of lung cell RNA expression data.
- Cluster the cells based on their expression profiles.
- Annotate cell types by comparing expression profiles with reference data.

## Data Description
The dataset consists of **22,418 genes** across **7,779 lung cells**. After filtering based on mitochondrial gene expression and gene counts, **7,098 cells** were retained for further analysis.

## Analysis Workflow

### 1. **Data Pre-processing**
The dataset was filtered to remove cells with high mitochondrial gene expression or extreme gene counts. A violin plot was used to visualize quality control metrics, and inappropriate cells were removed to ensure high-quality data for further analysis.

### 2. **Dimensionality Reduction and Clustering**
Using Principal Component Analysis (PCA), the data was reduced to a manageable number of dimensions, making it easier to identify patterns. We selected the top 6 principal components for further clustering and visualized the results using UMAP (Uniform Manifold Approximation and Projection).

### 3. **Cell Type Identification**
We identified specific gene markers for each cluster using differential gene expression analysis. The identified clusters were then compared with reference mouse RNA-seq data to annotate the cell types.

## Visualizations

1. **Violin Plot**: Displayed QC metrics such as RNA features and mitochondrial gene expression across the dataset to highlight filtering criteria.

   ![image](https://github.com/user-attachments/assets/e578a479-d62e-4288-bd6e-b1b2033f2ebb)


2. **UMAP Plot**: Visualized cell clustering into 13 distinct groups, corresponding to different cell types such as fibroblasts, monocytes, and macrophages.

   ![image](https://github.com/user-attachments/assets/5d37e6a3-d169-4ed7-891c-c9912c596ffc)


3. **FeaturePlot**: Highlighted differentially expressed genes, showing which genes are expressed in specific clusters, helping to identify cell types.

   ![image](https://github.com/user-attachments/assets/21dce010-c13e-436b-9d4b-f15df12e9b56)


## Results
The analysis identified several distinct lung cell types, each with unique gene expression patterns. Key findings include:
- Clear clustering of fibroblasts, monocytes, and macrophages.
- Specific gene markers like **Nox4** and **Dnah12** were expressed predominantly in certain clusters, providing insights into the role of different cell types.

## Conclusion
This scRNA-seq analysis successfully identified and clustered various lung cell types in an adult mouse based on their gene expression profiles. The approach allowed us to assign cell types to each cluster, enriching our understanding of lung cell composition in this sample.

## How to Reproduce
1. Download the dataset from 10X Genomics.
2. Set up the analysis environment.
3. Run the provided R markdown file (scRNA-seq.Rmd) to reproduce the analysis.

---
## Contributors
- **Reut Lev** (reutlev98)
- **Ye'ela Granot** (yeela8g)
- **Shir Ohayon** (shir677)
