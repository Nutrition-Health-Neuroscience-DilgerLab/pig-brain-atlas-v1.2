<div align="center">

# Piglet Brain MRI Atlas v1.2

**Averaged MRI brain template, 19 labeled regions, and tissue probability maps for the 4-week-old domestic piglet (*Sus scrofa domestica*)**

[![Atlas version](https://img.shields.io/badge/atlas-v1.2-2a9d8f?style=for-the-badge)](https://pigmri.illinois.edu/neuroimaging-resources)
[![Updated](https://img.shields.io/badge/updated-2016--12--12-4361ee?style=for-the-badge)](https://pigmri.illinois.edu/neuroimaging-resources)
[![Age](https://img.shields.io/badge/age-4%20wk-e76f51?style=for-the-badge)](#at-a-glance)
[![Regions](https://img.shields.io/badge/regions-19-9b72cf?style=for-the-badge)](#labeled-regions)
[![License](https://img.shields.io/badge/license-CC0%201.0-3fb950?style=for-the-badge)](LICENSE)

[![Paper](https://img.shields.io/badge/PLOS%20ONE-2014-ef8a62?style=flat-square)](https://doi.org/10.1371/journal.pone.0107650)
[![DOI](https://img.shields.io/badge/DOI-10.1371%2Fjournal.pone.0107650-blue?style=flat-square)](https://doi.org/10.1371/journal.pone.0107650)
[![PubMed](https://img.shields.io/badge/PubMed-25254955-326599?style=flat-square)](https://pubmed.ncbi.nlm.nih.gov/25254955/)
[![Format](https://img.shields.io/badge/format-NIfTI--1%20(gzip)-555?style=flat-square)](https://nifti.nimh.nih.gov/nifti-1)
[![Website](https://img.shields.io/badge/website-pigmri.illinois.edu-13294B?style=flat-square)](https://pigmri.illinois.edu/)
[![Cite](https://img.shields.io/badge/cite-CITATION.cff-f2c14e?style=flat-square)](CITATION.cff)

</div>

> **Newer versions are available.** [Version 2.1](https://github.com/Nutrition-Health-Neuroscience-DilgerLab/pig-brain-atlas-v2.1) (2023) covers 4- and 12-week-old pigs with 29 regions, four tissue classes, and FA templates. Use v1.2 only to reproduce earlier work.

## Overview

This repository holds version 1.2 of the averaged brain atlas of the 4-week-old piglet described in [Conrad et al. (2014)](https://doi.org/10.1371/journal.pone.0107650), built at the University of Illinois Urbana-Champaign by the Johnson and Dilger laboratories (Department of Animal Sciences) with the Biomedical Imaging Center at the Beckman Institute for Advanced Science and Technology. It was the starting reference for the 4-week atlas in [version 2.0](https://github.com/Nutrition-Health-Neuroscience-DilgerLab/pig-brain-atlas-v2.0).

Version 1.2 (12 December 2016) updated the tissue segmentation files of version 1.1, the original release. The files in `atlas/` are unpacked unchanged from the official download on the [Pig Imaging Group website](https://pigmri.illinois.edu/neuroimaging-resources), including its `ReadMe.txt`. The original archive is also attached to the [v1.2 release](https://github.com/Nutrition-Health-Neuroscience-DilgerLab/pig-brain-atlas-v1.2/releases/tag/v1.2).

## At a glance

| | 4-week-old atlas |
|---|---|
| Matrix (voxels) | 160 × 200 × 160 |
| Voxel size | 0.5 mm isotropic |
| Labeled regions | 19 |
| Tissue classes | gray matter, white matter, CSF (smoothed with a 1 mm kernel) |
| FA template | no |
| File format | gzipped NIfTI-1 (`.nii.gz`) |

## Contents

```
.
├── atlas/
│   └── Piglet_MRI_Atlas_V1.2/
│       ├── Piglet_Averaged_Brain.nii.gz         averaged T1-weighted template
│       ├── ROI_Combined.nii.gz                  all regions in one label image
│       ├── ROI_Labels.xlsx                      label number for each region
│       ├── ROI_Labels/<Region>.nii.gz           one binary mask per region
│       ├── Tissue_Probability_Maps/
│       │   └── smooth_1mm_{gray,white,csf}.nii.gz
│       └── ReadMe.txt                           original readme from the download
├── downloads/SHA256SUMS                         checksum of the original archive
├── ATLAS_SHA256SUMS                             checksum of every extracted file
├── CITATION.cff
├── LICENSE                                      CC0 1.0
└── README.md
```

The original `ReadMe.txt` names the images with a `.nii` extension; the files in the download are gzipped (`.nii.gz`), which standard neuroimaging software reads directly.

## Labeled regions

The label numbers come from `ROI_Labels.xlsx`.

| Label | Region | Label | Region |
|---:|---|---:|---|
| 1 | Caudate | 11 | Medulla |
| 2 | Cerebellum | 12 | Midbrain |
| 3 | Left cortex | 13 | Pons |
| 4 | Right cortex | 14 | Putamen and globus pallidus |
| 5 | Lateral ventricle | 15 | Hypothalamus |
| 6 | Third ventricle | 16 | Thalamus |
| 7 | Cerebral aqueduct | 17 | Olfactory bulb |
| 8 | Fourth ventricle | 18 | Corpus callosum |
| 9 | Left hippocampus | 19 | Internal capsule |
| 10 | Right hippocampus | | |

Later versions use different label numbers and split several regions into left and right, so label numbers are not interchangeable between versions.

## Usage

**Integrity check.** To confirm that the atlas files are unchanged, run the following from the `atlas/` folder:

```bash
shasum -a 256 -c ../ATLAS_SHA256SUMS
```

## Version history

| Version | Released | Ages | Regions | Notes |
|---|---|---|---|---|
| [2.1](https://github.com/Nutrition-Health-Neuroscience-DilgerLab/pig-brain-atlas-v2.1) | 2023-07-21 | 4 wk, 12 wk | 29 | Current release. |
| [2.0](https://github.com/Nutrition-Health-Neuroscience-DilgerLab/pig-brain-atlas-v2.0) | 2021-04-01 | 4 wk, 12 wk | 26 | Described in Fil et al. (2021). |
| **1.2** | 2016-12-12 | 4 wk | 19 | This repository. Updated tissue segmentation files. |
| 1.1 | 2014 | 4 wk | 19 | Original atlas files (Conrad et al., 2014). |

## Citation

Please cite the article that describes this atlas when using these files:

> Conrad, M. S., Sutton, B. P., Dilger, R. N., & Johnson, R. W. (2014). An in vivo three-dimensional magnetic resonance imaging-based averaged brain collection of the neonatal piglet (*Sus scrofa*). *PLoS ONE*, *9*(9), e107650. https://doi.org/10.1371/journal.pone.0107650

```bibtex
@article{conrad2014piglet,
  title   = {An in vivo three-dimensional magnetic resonance imaging-based averaged brain collection of the neonatal piglet (Sus scrofa)},
  author  = {Conrad, Matthew S. and Sutton, Bradley P. and Dilger, Ryan N. and Johnson, Rodney W.},
  journal = {PLoS ONE},
  volume  = {9},
  number  = {9},
  pages   = {e107650},
  year    = {2014},
  doi     = {10.1371/journal.pone.0107650}
}
```

## Contact

Questions about the atlases can be sent to Ryan N. Dilger, Department of Animal Sciences, University of Illinois Urbana-Champaign ([rdilger2@illinois.edu](mailto:rdilger2@illinois.edu)).

## License

The atlas files were released under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/), as stated in the original `ReadMe.txt`; the full text is in [`LICENSE`](LICENSE). You may use them for any purpose without restriction. Citing Conrad et al. (2014) is requested as good scholarly practice, not required by the license.
