# Mouse islet scRNA-seq analysis

This repository contains the scripts used to explore single-cell RNA sequencing (scRNA-seq) datasets from mouse pancreatic islets under control diet (CD) and high-fat diet (HFD) conditions.

The workflow is implemented in Python using [Scanpy](https://scanpy.readthedocs.io/) and covers quality control, data preprocessing, dimensionality reduction, clustering, cell-type annotation, reference-based label transfer, and pseudobulk count generation.

## Datasets

The current analysis notebook uses publicly available mouse pancreatic islet scRNA-seq data associated with the following GEO records:

- [GSE203151](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE203151)

Please refer to the GEO records and their associated publication for complete sample metadata, experimental design, and data-access information.

## Analyses included in this repository

1. scRNA-seq preprocessing, integration, clustering, and cell-type annotation
2. Differentially expressed gene (DEG) analysis
3. Gene set enrichment analysis (GSEA)
4. GPCR gene mapping and expression analysis
5. Data visualization and figure generation

## Cell populations

The workflow identifies the following major pancreatic cell populations:

- Alpha cells
- Beta-cell subpopulations
- Delta cells
- Gamma/PP cells
- Ductal cells
- Endothelial cells
- Macrophages
- Mesenchymal stromal cells

Cell-type annotations should be validated using multiple established marker genes and the biological context of the original study.

## Repository structure

```text
.
├── README.md
└── notebooks/
    ├── mouse_islet_scRNAseq_clustering.ipynb
    ├── mouse_islet_scRNAseq_DEG.ipynb
    ├── mouse_islet_scRNAseq_DE_Gpcrs.ipynb
    ├── mouse_islet_scRNAseq_gsea.ipynb
    └── mouse_islet_scRNAseq_plotting.ipynb
```

## Requirements

The analysis requires Python 3 and the following main packages:

```text
scanpy
anndata
pandas
numpy
matplotlib
seaborn
```

For reproducibility, record the exact package versions in an `environment.yml` or `requirements.txt` file.

## Usage

1. Download the required count matrices and metadata from GEO.
2. Update the input paths in the notebook.
3. Add the true biological sample identifiers and experimental conditions to `adata.obs`.
4. Run the notebook cells in order.


## Citation

If you use the datasets analyzed in this repository, please cite the original study associated with the GEO records. Add the project-specific manuscript citation here when available.

## Copyright

Dr Zekun Lyu

## License

Add the license governing reuse of the code in this repository, for example an MIT `LICENSE` file.
