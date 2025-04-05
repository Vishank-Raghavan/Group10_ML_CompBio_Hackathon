# Group10_ML_CompBio_Hackathon

Report: https://docs.google.com/document/d/1Nmy3iT_MZwg2wqBV7ITGvZCz9BvEhodtW2m-c8EE7OU/edit?usp=sharing

# How to Run - Hackathon_Script.ipynb
First, ensure that you have a conda environment for the required packages or have locally installed them via pip install; the conda environment provided by finetune.yml should work here as well, but has not been tested for this script. Next, run all cells in section 1. To run the rest of the code, it depends on which model and what encodings you are testing. For OHE, first run the second ProteinDataset cell and the cell after it, and then simply find the model you would like to run and run its class cell. Next, run the Train_Model function, the cor function to ensure early stopping works, and then find the cell that matches it name for the model = {Insert Model Name Here}.to(device). Alternatively, simply find a cell with a model run and change the model name to the one you wish to run. For ESM2 embeddings, make sure to run the gen_EMB function and generate both the training and test embeddings by running the fasta file cells and corresponding gen_emb cells. Then follow the same process as before but make sure you run the train_model_ESM function and cor_ESM function as the training and correlation calculations have a few differences here. For ensemble models, follow the cells under the Ensemble Methods header, and finally, for Active Learning, run the cells in that section. For making test set predictions with ESM embeddings, make sure you run the ProteinTestESMDataset class and load the embeddings by initializing the class. 

# How to Run - Query1Commands.ipynb
Simply run all cells in section 1 of the notebook. 

# How to Run - Finetuning_per_protein_Revised.ipynb
Notes: If the notebook does not render on GitHub, simply download it, and it should appear fine in an IDE. Second, this notebook has been adapted from [Schmirler et al.](https://www.nature.com/articles/s41467-024-51844-2), and the source notebook can be found [here](https://zenodo.org/records/12770310). 

First, either manually install all packages with the required versions in the notebook or set up a conda environment using the finetune.yml file in this GitHub repo. For model training and test result generation, simply run all cells in order until the active learning section at the bottom. To run the active learning section, you will need to generate 5 prediction results with a bagged set of predictions using different seeds in the train/validation split section. 
