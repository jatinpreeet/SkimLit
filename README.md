# SkimLit
# SKIMLIT : The purpose of this project is to make a NLP model to make medical abstracts easier to read.
## Replicating a deep learning model behind the 2017 revolutionary paper : PubMed 200k RCT: a Dataset for Sequenctial Sentence Classification in Medical Abstracts.https://arxiv.org/abs/1710.06071
## Model in this paper has an accuracy of 88% 


### Data : https://github.com/Franck-Dernoncourt/pubmed-rct


# Model experimented with it: 
1. Simple MultinomialNB(Naive Bayes) with TfidVectorizer -> 71%
   <img width="1334" alt="Screenshot 2024-07-13 at 12 17 10 PM" src="https://github.com/user-attachments/assets/d25ba086-e850-4f7b-9be6-61ca5387e5f2">
   <img width="327" alt="Screenshot 2024-07-13 at 12 18 54 PM" src="https://github.com/user-attachments/assets/5c586a17-cc9f-44e2-bf9c-53e7d3b1c9b7">

   
2. Conv1D with custom token embedding -> 79%
   <img width="826" alt="Screenshot 2024-07-13 at 12 20 11 PM" src="https://github.com/user-attachments/assets/5ae5c8ee-0771-4203-b786-bc6ae0e63025">
   <img width="335" alt="Screenshot 2024-07-13 at 12 21 48 PM" src="https://github.com/user-attachments/assets/7a36956d-d89c-43ea-a0ab-8e5a0c04af07">

3. Model with pretrained token embedding(Universal sentence embedding) -> 71.6%
   <img width="868" alt="Screenshot 2024-07-13 at 12 24 13 PM" src="https://github.com/user-attachments/assets/d4abfdae-c5a6-46fd-8139-fccb138409f6">
   <img width="666" alt="Screenshot 2024-07-13 at 12 23 47 PM" src="https://github.com/user-attachments/assets/c46824eb-4aa0-4c70-8115-a570333e1045">
   <img width="365" alt="Screenshot 2024-07-13 at 12 25 34 PM" src="https://github.com/user-attachments/assets/b3271a01-8e3b-464f-9678-68c7d52eba2e">

4. Conv1D with character embedding ->
   <img width="681" alt="Screenshot 2024-07-13 at 12 30 45 PM" src="https://github.com/user-attachments/assets/677bc6db-05e0-4f5b-a4e4-f9fa1d896b95">
   <img width="794" alt="Screenshot 2024-07-13 at 12 29 59 PM" src="https://github.com/user-attachments/assets/920ccf54-de05-41c2-90dd-d27d4e8667cd">

5. Model with hybrid embeddings ( char level embedding + token embedding) -> 74%
   <img width="1063" alt="Screenshot 2024-07-13 at 12 33 26 PM" src="https://github.com/user-attachments/assets/0f382073-e97d-467f-b7d9-e1b6027a3434">
   ![Unknown](https://github.com/user-attachments/assets/d3cc479a-7355-4077-8d2c-4516b450291e)

6. Model with hybrid embeddings ( char level embedding + custom token embedding) - > 75%
   <img width="1063" alt="Screenshot 2024-07-13 at 12 36 40 PM" src="https://github.com/user-attachments/assets/dab5c5b7-45d7-40be-a715-5f4d2b57f9bf">

7. Model with tribrid embeddings ( char level + token level + positional) -> 85%
   <img width="727" alt="Screenshot 2024-07-13 at 12 37 59 PM" src="https://github.com/user-attachments/assets/e5d4ba2c-366e-4b45-a6c2-a48876f82b4c">


   ##Our best model with tribidding embeddings and certain specific tuning got us at 85% accuracy which is close to the model accuracy in the original paper 88%


# some of the models results 
<img width="570" alt="Screenshot 2024-07-13 at 12 40 27 PM" src="https://github.com/user-attachments/assets/db00cb19-8b42-4c9d-afe5-268007188748">


   


   


