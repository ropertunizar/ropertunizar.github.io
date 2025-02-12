---
date: 2024-03-26
title: "SpectralWaste Dataset: Multimodal Data for Waste Sorting Automation"
venue: "IROS 2024"
authors:
  - name: "Sara Casao"
    url: "https://www.linkedin.com/in/sara-casao-martinez-5b49b9180"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
    notes: ["Joint first authors"]
  - name: "Fernando Peña"
    url: "https://ferpb.com"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
    notes: ["Joint first authors"]
  - name: "Alberto Sabater"
    url: "https://sites.google.com/unizar.es/alberto-sabater/"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
  - name: "Rosa Castillón"
    url: "https://www.linkedin.com/in/rosacastillon"
    affiliations: ["ATRIA Innovation"]
  - name: "Darío Suárez"
    url: "https://webdiis.unizar.es/~dario/"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
  - name: "Eduardo Montijano"
    url: "https://sites.google.com/unizar.es/eduardo-montijano"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
  - name: "Ana C. Murillo"
    url: "https://sites.google.com/unizar.es/anac"
    affiliations: ["DIIS-I3A, Universidad de Zaragoza"]
links:
  - name: "Paper"
    icon: "ai-ieee"
    url: "https://ieeexplore.ieee.org/document/10801797"
  - name: "Paper"
    icon: "ai-arxiv"
    url: "https://arxiv.org/abs/2403.18033"
  - name: "Data"
    icon: "ai-zenodo"
    url: "https://zenodo.org/records/10880544"
  - name: "Code (Dataset)"
    icon: "bi-github"
    url: "https://github.com/ferpb/spectralwaste-dataset"
  - name: "Code (Segmentation)"
    icon: "bi-github"
    url: "https://github.com/ferpb/spectralwaste-segmentation"
project: separa
slug: spectralwaste
keywords: ["hyperspectral-imaging", "semantic-segmentation", "recycling"]
description: Esta es una descripción corta de mi paper
image: smallteaser.png
---

<figure>
  <img src="teaser.png" alt="Descriptive caption">
</figure>

## Description

In this project, we introduce a dataset for waste segmentation, collected in a real waste processing facility using a multimodal imaging setup comprising an RGB camera and a hyperspectral camera. The data was captured with a true-to-life prototype of a conveyor belt, closely replicating real-world operating conditions. The waste streams were recorded as they arrived to the facility for initial classification, ensuring that the dataset accurately represents the materials encountered in the first stage of the sorting process.

For image acquisition, two synchronized line-scan cameras were used:

* RGB Camera: Teledyne DALSA Linea.
* Hyperspectral Camera: Specim FX17, capturing 224 contiguous spectral bands within the 900–1700 nm range.

The annotations focus on objects that pose operational challenges in automated waste sorting, directly impacting efficiency and reliability. Each class represents a material commonly responsible for disruptions, particularly machinery jams, which can halt the entire process until the obstruction is manually removed. The key problematic objects include:

* Film and basket: Large, rigid materials that clog conveyor belts.
* Video tape and filament: Long, flexible objects prone to entanglement with mechanical components.
* Trash bag: Closed waste bags requiring mechanical opening for proper sorting.
* Cardboard and paper: Valuable recyclable materials that should be redirected into separate recovery processes.

By providing high-resolution multimodal data under realistic conditions, this dataset supports the development of more robust waste identification and sorting models, aiming to improve recycling efficiency and minimize process interruptions.

## Code and Datasets

The raw SpectralWaste dataset can be accessed through the links below. For convenience, we provide a version containing only labeled images for easier download. The code to load and process this dataset is available on [GitHub][dataset-repo].

* Raw labeled dataset:
  * RGB and HSI images (105 GB): [OneDrive][raw-labeled-onedrive].
* Raw complete (labeled and unlabeled) dataset:
  * RGB images (3.8 GB): [OneDrive][raw-full-rgb-onedrive].
  * RGB and HSI images (1.3 TB): Please contact the [authors](mailto:fpena@unizar.es,acm@unizar.es).

For the paper, we use a preprocessed version of the labeled images, optimized for both reduced storage and faster training. The code to replicate the experiments using this version is available on [GitHub][segmentation-repo].

* Labeled RGB and HSI images (23 GB): [Zenodo][preprocessed-labeled-zenodo], [OneDrive][preprocessed-labeled-onedrive].
* Unlabeled RGB and HSI images (178 GB): [OneDrive][preprocessed-unlabeled-onedrive].

[dataset-repo]: https://github.com/ferpb/spectralwaste-dataset
[segmentation-repo]: https://github.com/ferpb/spectralwaste-segmentation

[preprocessed-labeled-zenodo]: https://zenodo.org/records/10880544
[preprocessed-labeled-onedrive]: https://unizares-my.sharepoint.com/:u:/g/personal/756012_unizar_es/EVJygVCmvs1BrCvA_WEtcIcBkUGbgsmN4fLaWGwr_lLJBw?e=lSPWxs
[preprocessed-unlabeled-onedrive]: https://unizares-my.sharepoint.com/:u:/g/personal/756012_unizar_es/Ea5ec2LtwoVOjlKfobsqbwsBTsgQMbIcnh_p0YbQvEH36A?e=vu4BHh
[raw-labeled-onedrive]: https://unizares-my.sharepoint.com/:f:/g/personal/756012_unizar_es/EkzyB3aciG1GncKAHUdh_sEB2Ch8kGwxLTyvLBHdKTiM_Q?e=feRBh6
[raw-full-rgb-onedrive]: https://unizares-my.sharepoint.com/:u:/g/personal/756012_unizar_es/EWFDxj3rv1JFnPFVLCd0ePwBV3hsps2nwX84nq3orIgHzw?e=wtXoXC

## BibTeX

```
@inproceedings{pena2024spectralwaste,
  title = {{SpectralWaste} Dataset: Multimodal Data for Waste Sorting Automation},
  author = {Casao, Sara and Pe{\~n}a, Fernando and Sabater, Alberto and Castill{\'o}n, Rosa and Su{\'a}rez, Dar{\'i}o and Montijano, Eduardo and Murillo, Ana C.},
  year = {2024},
  booktitle = {2024 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages = {5852-5858},
  doi = {10.1109/IROS58592.2024.10801797}
}
```

## Acknowledgements

This work was supported by DGA project T45 23R and by MCIN/AEI/ERDF/European Union NextGenerationEU/PRTR project PID2021-125514NB-I00. The authors thank the SEPARA project and all its partners: Ecoembes, Picvisa, PiperLab, Trienekens, Fundación GAIKER and Leitat.

<img src="/logos/aei-eu.png" style="width: 250px; display: block; margin: 0 auto">
