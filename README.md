# Rcpi  <a href="https://nanx.me/Rcpi/"><img src="https://i.imgur.com/v8lHCn9.png" align="right" alt="logo" height="180" width="180" /></a>

[![Build Status](https://travis-ci.org/road2stat/Rcpi.svg?branch=master)](https://travis-ci.org/road2stat/Rcpi)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/road2stat/rcpi?branch=master&svg=true)](https://ci.appveyor.com/project/road2stat/rcpi)
[![bioc](https://www.bioconductor.org/shields/years-in-bioc/Rcpi.svg)](https://bioconductor.org/packages/release/bioc/html/Rcpi.html#since)
[![downloads](https://www.bioconductor.org/shields/downloads/Rcpi.svg)](https://bioconductor.org/packages/stats/bioc/Rcpi/)

[BioC (Release)](https://www.bioconductor.org/packages/release/bioc/html/Rcpi.html) · [BioC (Development)](https://www.bioconductor.org/packages/devel/bioc/html/Rcpi.html) · [GitHub (Latest)](https://github.com/road2stat/Rcpi)

## Overview

Rcpi offers a molecular informatics toolkit with a comprehensive integration of bioinformatics and cheminformatics tools for drug discovery. For more information, please see our paper <[DOI:10.1093/bioinformatics/btu624](https://academic.oup.com/bioinformatics/article-lookup/doi/10.1093/bioinformatics/btu624)> ([PDF](https://nanx.me/papers/Rcpi.pdf)).

## Paper Citation

Formatted citation:

Dong-Sheng Cao, Nan Xiao, Qing-Song Xu, and Alex F. Chen. (2015). Rcpi: R/Bioconductor package to generate various descriptors of proteins, compounds and their interactions. _Bioinformatics_ 31 (2), 279-281.

BibTeX entry:

```
@article{Rcpi2015,
  author = {Cao, Dong-Sheng and Xiao, Nan and Xu, Qing-Song and Alex F. Chen.},
  title = {{Rcpi: R/Bioconductor package to generate various descriptors of proteins, compounds and their interactions}},
  journal = {Bioinformatics},
  year = {2015},
  volume = {31},
  number = {2},
  pages = {279--281},
  doi = {10.1093/bioinformatics/btu624},
  issn = {1367-4803},
  url = {http://bioinformatics.oxfordjournals.org/content/31/2/279}
}
```

## Installation

To install the `Rcpi` package:

```r
source("https://bioconductor.org/biocLite.R")
biocLite("Rcpi")
```

To make the package fully functional (especially the Open Babel related functions), we recommend installing the _Enhances_ packages by:

```r
source("https://bioconductor.org/biocLite.R")
biocLite("Rcpi", dependencies = c("Imports", "Enhances"))
```

Several dependencies of the Rcpi package may require some system-level libraries, check the corresponding manuals of these packages for detailed installation guides.

Browse the package vignettes: [[1](https://nanx.me/Rcpi/articles/Rcpi.html)], [[2](https://nanx.me/Rcpi/articles/Rcpi-quickref.html)] for a quick-start.

## Features

Rcpi implemented and integrated the state-of-the-art protein sequence descriptors and molecular descriptors/fingerprints with R. For protein sequences, the Rcpi package could

- Calculate six protein descriptor groups composed of fourteen types of commonly used structural and physicochemical descriptors that include 9920 descriptors.

- Calculate six types of generalized scales-based descriptors derived by various dimensionality reduction methods for proteochemometric (PCM) modeling.

- Parallellized pairwise similarity computation derived by protein sequence alignment and Gene Ontology (GO) semantic similarity measures within a list of proteins.

For small molecules, the Rcpi package could

- Calculate 307 molecular descriptors (2D/3D), including constitutional, topological, geometrical, and electronic descriptors, etc.

- Calculate more than ten types of molecular fingerprints, including FP4 keys, E-state fingerprints, MACCS keys, etc., and parallelized chemical similarity search.

- Parallelized pairwise similarity computation derived by fingerprints and maximum common substructure search within a list of small molecules.

By combining various types of descriptors for drugs and proteins in different methods, interaction descriptors representing protein-protein or compound-protein interactions could be conveniently generated with Rcpi, including:

- Two types of compound-protein interaction (CPI) descriptors

- Three types of protein-protein interaction (PPI) descriptors

Several useful auxiliary utilities are also shipped with Rcpi:

- Parallelized molecule and protein sequence retrieval from several online databases, like PubChem, ChEMBL, KEGG, DrugBank, UniProt, RCSB PDB, etc.

- Loading molecules stored in SMILES/SDF files and loading protein sequences from FASTA/PDB files

- Molecular file format conversion

The computed protein sequence descriptors, molecular descriptors/fingerprints, interaction descriptors and pairwise similarities are widely used in various research fields relevant to drug disvery, primarily bioinformatics, cheminformatics, proteochemometrics, and chemogenomics.

## Contribute

To contribute to this project, please take a look at the [Contributing Guidelines](https://github.com/road2stat/Rcpi/blob/master/CONTRIBUTING.md) first. Please note that this project is released with a [Contributor Code of Conduct](https://github.com/road2stat/Rcpi/blob/master/CONDUCT.md). By participating in this project you agree to abide by its terms.
