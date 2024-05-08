# Project Execution

This repository hosts the code used to reproduce the findings of our research on multi-modal analysis for Alzheimer's Disease detection using clinical, imaging, and genetic data. The methodology is aligned with the original MADDi paper.
This repository contains all the code necessary to recreate this project and therefore the original MADDi paper.

## Prerequisites

- Python 3.7 or higher

## Installation

The package dependencies are located in /general/requirements.txt file and can be installed from there

### Data Download Instructions

To access the ADNI dataset, follow these steps:

1.   **Complete the Data Use Agreement form**: The  [ADNI Data Use Agreement](https://ida.loni.usc.edu/collaboration/access/appLicense.jsp) can be accessed directly.
2.   **Apply for Access**: Submit an application for accessing the ADNI dataset. This includes providing your affiliation and the use case for the data.
3. **Download Data**: Once the access request is approved. Users can log in to the LONI website to access and download ADNI datasets. Include study, imaging, and genetic data.

### Data Description

The dataset used in this study comprises multi-modal data sourced from ADNI (Alzheimer's Disease Neuroimaging Initiative). Given the confidential nature of this data, detailed charts and visualizations cannot be provided. Below is a general description of the types of data included, based on the methodologies outlined in the MADDi paper:

1. **Imaging Data**:
   - Consists of cross-sectional MRI scans from the baseline screenings of participants.
   - Images have been standardized by ADNI with GradWarp, B1 Correction, and N3 preprocessing steps.
   - Three slices of MRI images are included per patient, resized to 72x72 pixels.

2. **Genetic Data**:
   - Consists of whole genome sequencing (WGS) performed by Illumina's non-Clinical Laboratory Improvement Amendments (non-CLIA) process.
   - The initial dataset is reduced down to approximately 15,000 SNPs during preprocessing.
   - Data is in the form of large VCF files curated by ADNI in 2014.

3. **Clinical Data**:
   - Consists of initial assessments from neurological exams, cognitive tests, and demographic information.
   - 29 features
  
### Data Preprocessing
#### Execute the following files to preprocess that data once downloaded.
1. [Initial Preparation](https://github.com/tomasanthony/cs598-project/blob/main/general/diagnosis_making.ipynb)
2. [Clinical Preprocessing](https://github.com/tomasanthony/cs598-project/tree/main/preprocess_clinical)
3. [Genetic Preprocessing](https://github.com/tomasanthony/cs598-project/tree/main/preprocess_genetic)
4. [Image Preprocessing](https://github.com/tomasanthony/cs598-project/tree/main/preprocess_images)

### Training
The data, once preprocessed, can be uploaded into a Cloud Computing environment of choice or alternatively, the training can be done locally on a machine with a capable GPU.
Google Colab was used in this project.

The [final notebook](https://github.com/tomasanthony/cs598-project/blob/main/Team_112.ipynb) can then be executed to perform final data preprocessing and model training. 
