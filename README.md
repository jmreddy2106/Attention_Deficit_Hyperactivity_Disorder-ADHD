# Attention_Deficit_Hyperactivity_Disorder--ADHD-

This project aimed to detect Attention Deficit Hyperactivity Disorder (ADHD)/Control childern between 7-12 and they diagnosed by an experienced psychiatrist to DSM-IV criteria, and have taken Ritalin for up to 6 months. The data source from [EEG DATA FOR ADHD/CONTROL CHILDREN](https://ieee-dataport.org/open-access/eeg-data-adhd-control-children). To detect ADHD/Control, various machine learning teechniques are used which includes data preprocessing, feature selection technques. Since the dataset is imbalance, different ensemble algorithm techniques like Random Forest, XGBoost, and Gaussina Mixture Models (GMM) are implemented to detect ADHD/Control.

### Steps:
1. Extracted .mat files and converted into pandas dataframes

2. Asigned the feature names as per the documentation as as follows:
  - `Fp1`,`Fp2`,`F3`,`F4`,`C3`,`C4`,`P3`,`P4`,`O1`,`O2`,`F7`,`F8`,`T7`,`T8`,`P7`,`P8`,`Fz`,`Cz`,`Pz`, `class` (ADHD/Control)
  
3. Created the subsets of the features as below:

Feature Selection

=================

- Label the dataset ADHD - 1 and Control - 0
- Data sepration based on the regions
- based on the regions
    - Frontal (F)
    - Central (C)
    - Parietal (P)
    - Temporal (T)
    - Ocipital (O)
- Right Hemisphere ( `Fp2`,`F4`,`F8`, `C4`,`T4`, `P4`, `T6`, `O2` )
- Left Hemisphere ( `C3`, `T3`, `Fp1`, `F3`, `F7`, `P3`, `T5` , `O1` )
- Combionatin of CFO
- Combionatin of PT
- Combionatin of FOP
- Combionatin of CPT
- Combionatin of FCPTO

4. Constructed machine leanring models Randomforest and XGBoost and conread the various metrics like `Precision`, `Recall`, `Accuracy` and `F1-Score`.
