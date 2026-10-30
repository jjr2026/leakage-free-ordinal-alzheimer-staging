# Leakage-Free Ordinal Deep Learning for Alzheimer Disease Staging from Structural Magnetic Resonance Imaging with Quantitative Attention Mapping

Code for the paper by **Jami Janardhanarao, Somaraju Mouli and Chappa Ramesh**
(submitted to the *International Journal of Imaging Systems and Technology*, Wiley).

The study classifies three Clinical Dementia Rating (CDR) stages (Non-Demented, Very Mild, Mild/Moderate) from structural MRI of the OASIS-1 cohort using subject-level five-fold cross-validation, an ordinal formulation, quantitative Grad-CAM attention mapping, and an external validation on OASIS-3 with the model and decision rule fixed in advance.

## Notebooks

| Notebook | Contents |
|---|---|
| `Paper1_multistage.ipynb` | Main experiments on OASIS-1: data loading and preprocessing, leakage-free (subject-level) vs leaky (slice-level) cross-validation, standard vs ordinal models, cut-off selection, statistical tests, augmentation and class-imbalance strategies, and Grad-CAM region analysis |
| `Paper1_Revision_Analyses.ipynb` | Additional analyses: confusion matrices and cumulative AUCs (R1), region-occlusion control (R2), repeated cross-validation with extra seeds (R3), age as a confounder (R4), and the Figure 4 Grad-CAM drawing (R5) |
| `OASIS3_External_Validation_Paper1.ipynb` | External validation on OASIS-3: session selection, scan download, registration to the OASIS-1 template, preprocessing, and prediction with the five fixed models (no training or tuning on OASIS-3) |

## Requirements

Python 3 with TensorFlow/Keras, scikit-learn, NumPy, pandas, nibabel and matplotlib. The experiments were run on Google Colab with an NVIDIA T4 GPU. The OASIS-3 notebook also uses ANTs (installed within the notebook).

## Data

No imaging or clinical data are included in this repository. The OASIS-1 and OASIS-3 datasets are available from the OASIS project (https://sites.wustl.edu/oasisbrains/) to researchers who accept the OASIS Data Use Agreement. To run the notebooks, download the data yourself and set the paths in the *Settings* cell of each notebook. Login details for OASIS-3 downloads are read from Colab Secrets and are never stored in the code.

## License

MIT License (see `LICENSE`).
