# MIMIC-IV
A report on the dynamic nature of ECG acquisition in the MIMIC dataset.

<span style='font-family: Times; font-size: 2em;'>MIMIC v. 2.2 Database Dynamic Exploratory Data Analysis</span>


**Veronica Ramirez-Lopera** 

### Objectives: 
#### Main objective:
-To assess whether the MIMIC-IV database contains sufficient sequential ECGs to support a study 
on the dynamic aging of the heart in heart failure patients.

#### Secondary objectives:
1. To analyze the timing of ECGs during each hospitalization.
1. To visualize patient distribution by ECG frequency and hospitalization count.
1. To describe a plan for the research protocol modifications according to the ECG data.

### **Table of contents**
- [Introduction](#introduction)
- [Package Requirements](#package_requirements)
- [Data importing](#importing)
- [Data filtering and visualization](#filtering)
- [Conclusions and plan](#conclusions)
- [References](#references)

## Introduction <a name='introduction'></a>
MIMIC-IV is a freely available electronic health record (EHR) dataset encompassing a decade of patient information (2008-2019) from Beth Israel Deaconess Medical Center [1]. It surpasses its predecessor, MIMIC-III, with a better structure and additional patient information [2, 3].

The dataset draws upon two primary sources: a comprehensive hospital-wide EHR system and an ICU-specific clinical information system [1]. Rigorous de-identification procedures ensure patient privacy while preserving the data's scientific integrity.

It includes vital signs, diagnoses, medications, procedures, and de-identified clinical notes [1]. Researchers leverage MIMIC-IV to investigate disease progression, train machine learning models, and develop clinical decision support tools [1, 2].

As a result, null dates of death indicate the patient was alive at least up to that time point. Inferences regarding patient death beyond one year cannot be made using MIMIC-IV (as per the PhyioNet website) [2]. The majority of patient death information is acquired from hospital records when the individual dies within the BIDMC or an affiliated institute.

MIMIC-IV also offers a dedicated module: MIMIC-IV ECG. This subset focuses specifically on diagnostic electrocardiograms (ECGs) [2]. It includes approximately 800,000 10-second ECG recordings from nearly 160,000 unique patients. Each ECG utilizes 12 leads and is sampled at 500 Hz [3].


## Package requirements <a name='package_requirements'></a>

Notes: 

1- You need to install gcloud if you haven't already. Alternatively, you can use the provided csv files that contain the data.


Conclusions and plan

    The MIMIC database contains a significant number of sequential ECGs recorded at various times of an individuals life.
    There are 6,400 patients with ECGs showing a time gap of more than one year between recordings.
    Aging profiles could be analyzed for patients, especially those diagnosed with heart failure. While this analysis won't establish causation between the chronic disease and aging, it can provide insights into how heart failure impacts biological age, as estimated using deep learning techniques.

Possible Plan Modification:

    We could analyze the heart profile changes over a one-year period for patients diagnosed with heart failure and compare these changes to a three-year mortality rate. Although we cannot establish causality due to the lack of information on other exposures between hospitalizations, this approach could offer insights into how heart aging progresses in this population. Additionally, it might reveal whether a greater difference in aging profiles is associated with mortality among hospitalized patients.

References

    Johnson, Alistair, et al. "MIMIC-IV: A freely accessible electronic health record dataset." Schnpj (2021): 36596836. PubMed MIMIC-IV v2.2. PhysioNet
    Johnson, A., Bulgarelli, L., Pollard, T., Horng, S., Celi, L. A., & Mark, R. (2023). MIMIC-IV (version 2.2). PhysioNet. https://doi.org/10.13026/6mm1-ek67.
    Gow, B., Pollard, T., Nathanson, L. A., Johnson, A., Moody, B., Fernandes, C., Greenbaum, N., Waks, J. W., Eslami, P., Carbonati, T., Chaudhari, A., Herbst, E., Moukheiber, D., Berkowitz, S., Mark, R., & Horng, S. (2023). MIMIC-IV-ECG: Diagnostic Electrocardiogram Matched Subset (version 1.0). PhysioNet. https://doi.org/10.13026/4nqg-sb35.
    Fan J, Li X, Yu X, Liu Z, Jiang Y, Fang Y, et al. Global Burden, Risk Factor Analysis, and Prediction Study of Ischemic Stroke, 1990–2030. Neurology [Internet]. 2023 Jul 11 [cited 2024 Jun 30];101(2). Available from: https://www.neurology.org/doi/10.1212/WNL.0000000000207387
    Yang X, Gong Y, Waheed N, March K, Bian J, Hogan WR, et al. Identifying Cancer Patients at Risk for Heart Failure Using Machine Learning Methods. AMIA Annu Symp Proc. 2019;2019:933-41.


