# Plant-DTI Version 1.0
####   Copyright © 2022 Center for Agricultural Systems Biology
####   Authorship and citation: Ruengsrichaiya B., Nukoolkit C., Kalapanulak S. and Saithong T., (202x) Plant-DTI: Extending the landscape of TF protein and DNA interaction in plants by a machine learning-based approach. xxxxx., xx, xxx. (in preperation).
####   Contact: bhukrit.r@mail.kmutt.ac.th
----------------------------------------------------------------------------------------------------------------

This folder provided stand-alone of Plant-DTI model version 1 in .sav file and jupyter notebook for predicting DNA Binding Domain (DBD)- TF Binding site (TFBS) interaction using the model.

Users can download this folder to run code provided.

To predict the DBD-TFBS interactions, the Plant-DTI is also implemented as a web application tool and freely available at https://bml.kmutt.ac.th/Plant-DTI.

## Prerequisite install
To run code provided in this folder requires:

- python >= 3.6
- pandas module 
- numpy module
- Biopython Seq module
- scikit-learn module VERSION 0.23.2
- pickle module

## Model
This folder contains Plant-DTI models which including: 
- Random within models (RW) are avaiable for TFBS length range from 7-15 bp.
- Random pairs models (RP) are avaiable for TFBS length range from 7-14 bp.
- PlantDTI_models_availability.csv: Information of model aviability for each length and DBD type which required for Plant-DTI prediction.
- TFBS_base_preference: this folder contains TFBS base preference for particular model length, which required for represent TFBS sequence used in Plant-DTI.

## Result
Predicted DBD-TFBS interaction results will be generated in this folder.

## Plant-DTI_predict_example.ipynb
This code is example for predicting multiple queries of DBD-TFBS interactions using Plant-DTI. 
User have to define INPUT DBD-TFBS interaction probability for Plant-DTI prediction.

Result from model prediction will be generated in Result folder.

## example_input.csv
Example of multiple INPUT queries of DBD-TFBS interactions.
INPUT file columns must including:
- DBD_seq: DNA Binding Domain (DBD) of Transcription Factor (TF) protein sequence.
- pfam_name: DBD type based on Pfam name withih Plant-DTI coverage.
	['bZIP_1', 'GATA', 'HLH', 'SBP', 'zf-Dof', 'zf-C2H2', 'AP2' 
	AT_hook', 'B3', 'CSD', 'DUF573', 'EIN3', 'Homeobox','MADF_DNA_bdg'
	'Myb_DNA-binding', 'NAM', 'TCP', 'WRKY', 'CG-1','GRAS', 
	'HMG_box', 'DUF260', 'E2F_TDP', 'DUF822', 'SRF-TF', 'FAR1']

- TFBS_seq: Posible binding region of DNA or TFBS which have length 7 to 15 bp
- len_TFBS: length of TFBS which have length 7 to 15 bp

Result from model prediction will be generated in Result folder.


