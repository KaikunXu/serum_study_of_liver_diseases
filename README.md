# Serum Study of Liver Diseases

[![DOI:10.1016/j.mcpro.2023.100574](https://img.shields.io/badge/DOI-10.1016%2Fj.mcpro.2023.100574-blue.svg)](https://doi.org/10.1016/j.mcpro.2023.100574)

 Link to repository: [github.com/PHOENIXcenter/SerumStudyOfLiverDiseases](https://github.com/PHOENIXcenter/SerumStudyOfLiverDiseases)
+ Summary of scripts used for feature selection and machine learning in the project
+ MS-based proteome data are from two independent cohort:

|    **Cohort**     | **HC (Healthy Control)** | **CHB (Chronic Hepatitis B)** | **LC (Liver Cirrhosis)** | **HCC (Hepatocellular Carcinoma)** |
| :---------------- | :----------------------- | :--------------------------------- | :----------------------- | :--------------------------------- |
| Discovery cohort (n=125) | 21 | 29 | 29 | 46 |
| Validation cohort (n=75) | 15 | 15 | 15 | 30 |

## Contents

| Script                                        | Description                                                  |
| :-------------------------------------------- | :----------------------------------------------------------- |
| [Feature_Importance.py](Feature_Importance.py)   | Contains feature selection part. we used the LASSO model to executing feature selection, randomly select 80% of the samples each time to build a total of 500 sub-models, and chose proteins selected in at least 10% of the sub-models as candidate protein features. |
| [Classifier_Model.py](Classifier_Model.py)       | Contains machine learning modeling and performance evaluation part. We separately evaluated the performance of 6 classical machine learning models (SVM, Ridge, KNN, Naïve Bayes, Decision Tree and Random Forest) in each pairwise comparisons using corresponding candidate markers in both 5-fold discovery cohort and independent validation cohort. The main evaluation index are F1-score and AUROC. |
| [Model_Visualization.py](Model_Visualization.py) | Contains visualization of machine learning models, including confusion matrix and ROC curve of both 5-fold discovery cohort and validation cohort. |

## Data Availability

The complete serum proteomics data and clinical data are available from the authors upon reasonable request due to the need to maintain patient confidentiality.

The mass spectrometry proteomics data have been deposited to the ProteomeXchange Consortium (http://proteomecentral.proteomexchange.org) via the iProX partner repository with the dataset identifier PXD034201.

## Workflow of Machine Learning

![Workflow of machine learning modeling](https://github.com/PHOENIXcenter/SerumStudyOfLiverDiseases/blob/main/Workflow_of_machine_learning_modeling.png)

## Citation

**Text Format:**
> Xu, M., Xu, K., Yin, S., Chang, C., Sun, W., Wang, G., Zhang, K., Mu, J., Wu, M., Xing, B., Zhang, X., Han, J., Zhao, X., Wang, Y., Xu, D., & Yu, X. (2023). In-depth serum proteomics reveals the trajectory of hallmarks of cancer in hepatitis B virus–related liver diseases. *Molecular & Cellular Proteomics*, 22(7), 100574. https://doi.org/10.1016/j.mcpro.2023.100574

**BibTeX Format:**
```bibtex
@article{xu2023indepth,
  title={In-depth serum proteomics reveals the trajectory of hallmarks of cancer in hepatitis B virus--related liver diseases},
  author={Xu, Meng and Xu, Kaikun and Yin, Shangqi and Chang, Cheng and Sun, Wei and Wang, Guannan and Zhang, Kai and Mu, Jing and Wu, Mingxuan and Xing, Baocai and Zhang, Xiaomei and Han, Jinyu and Zhao, Xiaohang and Wang, Yajie and Xu, Danke and Yu, Xiaobo},
  journal={Molecular \& Cellular Proteomics},
  volume={22},
  number={7},
  pages={100574},
  year={2023},
  publisher={Elsevier},
  doi={10.1016/j.mcpro.2023.100574}
}
