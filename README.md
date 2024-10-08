# MA_DTA_Thesis_Marija_Kliocaite

The repository is structured in the following way:

Readme.md - information about the repository
Marija_Kliocaite_MA_DTA_Thesis.pdf - the completed thesis in PDF format.

BERT_RoBERTa_Baselines -- consists of 3 notebooks with baseline experiments of BERT and RoBERTa models on three different seeds. The back-translated dataset is obtained at the start of each notebook. The models in these notebooks are trained on half of the gold standard data, complete gold standard data and augmented (through back-tranlsation) gold standard data. All files necessary for running the code, as well as those generated as a result, are located in the same directory.

Baseline_Figures -- Consists of two notebooks.
 1. Preprocessing_data_baseline_MA_THESIS.ipynb -- consists of code exploring the dataset (including the selection of representative examples for the future GPT-based generation). Additionally, a SVC model is trained on the data to establish an additional classical ML baseline.
 2. FIGURES_FOR_THE_PAPER.ipynb -- consists of the code generating figures that are included in the paper. The datasets for the figures are also included in the same directory.

Confusion_matrices -- consists of 1 notebook and 5 folders. The notebook shows the code for the making of the visualizations. Each folders consists of .png files with confusion matrices: 
 1. baseline_seed_1 -- results from BERT_ROBERTA_MA_THESIS.ipynb
 2. baseline_seed_2 -- results from seed2_BERT_ROBERTA_MA_THESIS.ipynb
 3. baseline_seed_3 -- results from seed3_BERT_ROBERTA_MA_THESIS.ipynb
 4. GPT_BERT -- results from BERT models (first half) from GPT_Data_Classification/GPT_DATA_BERT_ROBERTA.ipynb
 5. GPT_RoBERTa -- results from RoBERTa models (second half) from GPT_Data_Classification/GPT_DATA_BERT_ROBERTA.ipynb

GPT_4o_mini_Data_Generation_and_Prep -- consists of 2 notebooks and all of the GPT-generated datasets, as well as the versions merged with the gold standard data.
 1. GPT-4o-mini.ipynb -- consists of the code used for generating the data. The API key used for this notebooks was replaced. The notebooks produces all the .csv files starting with "generated_tweets". Role 5 corresponds to role 1 with news articles.
 2. GPT_DATA_PREP.ipynb -- consists of the code for parsing and concatenating the generated data with a slice of gold standard data. Also, typicality is calculated in the same notebook. The code requires all of the files starting with "generated_tweets" to run, and produces the datasets used for the subsequent training of models. These files start with "gsd_gpt" or "half_gsd_half_gpt".

GPT_Data_Classification -- consists of 2 notebooks. 
 1. GPT_DATA_BERT_ROBERTA.ipynb -- the notebook where BERT and RoBERTa models are trained on all of the GPT-generated datasets with half of the GSD. These datasets (acquired in directory "GPT_4o_mini_Data_Generation_and_Prep") are included in the folder.
 2. Full_GSD_GPT_DATA_BERT_ROBERTA.ipynb -- the notebook where BERT and RoBERTa are trained on full GSD combined with the augmented data.

Thesis_Paper -- consists of all of files related to the project created in Overleaf.
