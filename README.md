## pyCERR-Notebooks

This repository provides notebooks for various use cases of pyCERR. These include 
* Organizing longitudinal, multi-modal image metadata
* IBSI-1 and IBSI-2 compatible radiomics
* RTDOSE dosimetry / DVHfeatures
* Infering image segmentation, registration using AI models

## Notebooks by topic

Notebooks are grouped into numbered topic folders (roughly beginner to advanced). Each can be opened directly in Google Colab via the badge at its top.

Shared inputs live at the repo root: `settings/`, `radiomics_settings/`, `radiomics_features/`.

## Getting started — load & visualize

`01_getting_started/`

| Notebook | Description |
|----------|-------------|
| [`load_visualize_scan_seg_ex1.ipynb`](01_getting_started/load_visualize_scan_seg_ex1.ipynb) | Load DICOM and view scan + segmentation |
| [`batch_visualize_scan_seg_ex1.ipynb`](01_getting_started/batch_visualize_scan_seg_ex1.ipynb) | Visualize scan + segmentation over a batch |
| [`animate_viewer.ipynb`](01_getting_started/animate_viewer.ipynb) | Animate / scroll through the viewer |
| [`copy_seg_to_scan.ipynb`](01_getting_started/copy_seg_to_scan.ipynb) | Copy a segmentation between scans |

## Data import (DICOM / NIfTI / XNAT)

`02_data_import/`

| Notebook | Description |
|----------|-------------|
| [`download_data_from_xnat.ipynb`](02_data_import/download_data_from_xnat.ipynb) | Pull data from an XNAT server |
| [`xnat2pycerr.ipynb`](02_data_import/xnat2pycerr.ipynb) | XNAT → pyCERR planC |
| [`xnat2pycerr_20251020.ipynb`](02_data_import/xnat2pycerr_20251020.ipynb) | XNAT pull + SMIT rectal segmentation |

## Auto-segmentation (deep-learning models)

`03_autosegmentation/`

| Notebook | Description |
|----------|-------------|
| [`ai_seg_inference_ex1.ipynb`](03_autosegmentation/ai_seg_inference_ex1.ipynb) | Generic AI segmentation inference template |
| [`ai_seg_adc_inference_ex1.ipynb`](03_autosegmentation/ai_seg_adc_inference_ex1.ipynb) | AI segmentation on ADC (MR) images |
| [`autosegment_patient_outline.ipynb`](03_autosegmentation/autosegment_patient_outline.ipynb) | Patient outline (body) segmentation |
| [`autosegment_CT_HeadAndNeck_OARs.ipynb`](03_autosegmentation/autosegment_CT_HeadAndNeck_OARs.ipynb) | CT head & neck OARs (DeepLab) |
| [`autosegment_CT_Heart_OARs.ipynb`](03_autosegmentation/autosegment_CT_Heart_OARs.ipynb) | CT heart sub-structure OARs (DeepLab) |
| [`autosegment_CT_Lung_OARs.ipynb`](03_autosegmentation/autosegment_CT_Lung_OARs.ipynb) | CT lung OARs (DeepLab) |
| [`autosegment_MR_Prostate_OARs.ipynb`](03_autosegmentation/autosegment_MR_Prostate_OARs.ipynb) | MR prostate OARs |
| [`autosegment_CT_HN_SMIT.ipynb`](03_autosegmentation/autosegment_CT_HN_SMIT.ipynb) | CT head & neck (SMIT) |
| [`autosegment_CT_HeartSubStruct_SMIT.ipynb`](03_autosegmentation/autosegment_CT_HeartSubStruct_SMIT.ipynb) | CT heart sub-structures (SMIT) |
| [`autosegment_CT_Lung_OARs_SMIT.ipynb`](03_autosegmentation/autosegment_CT_Lung_OARs_SMIT.ipynb) | CT lung OARs (SMIT) |
| [`autosegment_CT_Lung_GTV_SMIT.ipynb`](03_autosegmentation/autosegment_CT_Lung_GTV_SMIT.ipynb) | CT lung GTV (SMIT) |
| [`autosegment_MR_Rectum_GTV_SMIT.ipynb`](03_autosegmentation/autosegment_MR_Rectum_GTV_SMIT.ipynb) | MR rectum GTV (SMIT) |
| [`MR_HN_Nodule_SMIT_demo.ipynb`](03_autosegmentation/MR_HN_Nodule_SMIT_demo.ipynb) | MR head & neck nodule (SMIT) demo |
| [`autosegment_installer_CT_Heart_OARs.ipynb`](03_autosegmentation/autosegment_installer_CT_Heart_OARs.ipynb) | CT heart OARs via model_installer |
| [`SBG_autosegment_CT_Heart_OARs.ipynb`](03_autosegmentation/SBG_autosegment_CT_Heart_OARs.ipynb) | CT heart OARs on the Seven Bridges platform |

## Image registration & QA

`04_registration/`

| Notebook | Description |
|----------|-------------|
| [`deformable_image_registration_using_ANTS.ipynb`](04_registration/deformable_image_registration_using_ANTS.ipynb) | Deformable registration with ANTs |
| [`auto_register_segment_MR_Pancreas_OARs.ipynb`](04_registration/auto_register_segment_MR_Pancreas_OARs.ipynb) | Register then segment MR pancreas OARs |
| [`TG211_metrics.ipynb`](04_registration/TG211_metrics.ipynb) | AAPM TG-211 registration-QA metrics |

## Image preprocessing & filtering

`05_preprocessing/`

| Notebook | Description |
|----------|-------------|
| [`n4_bias_field_correct.ipynb`](05_preprocessing/n4_bias_field_correct.ipynb) | N4 bias-field correction |
| [`image_filters_lung_ct.ipynb`](05_preprocessing/image_filters_lung_ct.ipynb) | IBSI-2 image filters / texture maps |

## Radiomics — feature extraction

`06_radiomics_extraction/`

| Notebook | Description |
|----------|-------------|
| [`extractRadiomics.ipynb`](06_radiomics_extraction/extractRadiomics.ipynb) | Extract radiomics from a single dataset |
| [`batch_extract_radiomics_ex1.ipynb`](06_radiomics_extraction/batch_extract_radiomics_ex1.ipynb) | Batch radiomics extraction |
| [`batch_extract_radiomics_lung_ct.ipynb`](06_radiomics_extraction/batch_extract_radiomics_lung_ct.ipynb) | Batch radiomics extraction (lung CT) |
| [`analyzing_image_texture_using_pycerr.ipynb`](06_radiomics_extraction/analyzing_image_texture_using_pycerr.ipynb) | Texture-feature analysis |

## Radiomics — validation & comparison

`07_radiomics_validation/`

| Notebook | Description |
|----------|-------------|
| [`test_ibsi2_compatibility.ipynb`](07_radiomics_validation/test_ibsi2_compatibility.ipynb) | IBSI-2 reference compliance check |
| [`compare_pycerr-pyrad.ipynb`](07_radiomics_validation/compare_pycerr-pyrad.ipynb) | Compare pyCERR vs pyradiomics |

## Radiomics — analysis & modeling

`08_radiomics_analysis/`

| Notebook | Description |
|----------|-------------|
| [`Radiomics_network_based_clustering.ipynb`](08_radiomics_analysis/Radiomics_network_based_clustering.ipynb) | Network-based K-means clustering |
| [`EBIC_graphical_lasso.ipynb`](08_radiomics_analysis/EBIC_graphical_lasso.ipynb) | Graphical-lasso network model (EBIC) |

## Functional / quantitative imaging

`09_functional_imaging/`

| Notebook | Description |
|----------|-------------|
| [`extract_semi-quantitaive_dce-mri_features.ipynb`](09_functional_imaging/extract_semi-quantitaive_dce-mri_features.ipynb) | Semi-quantitative DCE-MRI features |

## Outcomes modeling (dosimetric)

`10_outcomes_modeling/`

| Notebook | Description |
|----------|-------------|
| [`normal_tissue_complication_probability.ipynb`](10_outcomes_modeling/normal_tissue_complication_probability.ipynb) | NTCP modeling |

## Treatment planning (IMRT)

`11_treatment_planning/`

| Notebook | Description |
|----------|-------------|
| [`imrtp_optimization_example.ipynb`](11_treatment_planning/imrtp_optimization_example.ipynb) | IMRT beamlet fluence-map optimization (pyCERR port of CERR's runOptimExample) |
