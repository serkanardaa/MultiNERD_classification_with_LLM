# MultiNERD_classification_with_LLM
 A Named Entity Recognition (NER) project with MultiNERD dataset using LLM.
 
 In this project, I have used  MultiNERD dataset for a token classification task called Named Entity Recognition (NER). The dataset can be analysed via following link:
 https://huggingface.co/datasets/Babelscape/multinerd?row=17
 
 The goal of the project was processing the dataset and using processed data as data source for fine-tuning an LLM model, which was bert-base-cased as my choice. The model can be analysed via following link:
 https://huggingface.co/bert-base-cased
 
 The project consisted 2 systems using different version of the dataset.
 
 System A: non-english tokens.
 In this system, I filtered MultiNERD dataset such that it will contain only english tokens. After that, the chosen LLM was trained on it.
 
 System B: non-english, five entity tokens.
 In this system additional to the same non-english token filtering I did in system A, I also set labels of entities existing in dataset except following entities:
 PERSON(PER), ORGANIZATION(ORG), LOCATION(LOC), DISEASES(DIS), ANIMAL(ANIM)
 
 The training was done in Google Colab using a T4-GPU.
 
# How To Run?

The whole project was implemented in Token Classification on MultiNERD.ipynb file. The required system packages and dependencies can be imported via requirements.txt file.
In order to interact with the hugging face hub, a login might be needed.

A brief summary of main findings and limitations can be read from Main findings and limitations.docx document.