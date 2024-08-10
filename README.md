# The Learning Agency Lab - PII Data Detection with DeBERTa

## Overview
The goal of this competition is to develop a model for detecting personally identifiable information (PII) in student writing, automating the process to lower the cost of releasing educational datasets. This is a text classification task, 'Named Entity Recognition' (NER). The project aims to develop a machine learning model capable of detecting Personally Identifiable Information (PII) within student essays. By leveraging the DeBERTa model, this task focuses on automating PII detection to facilitate the safe release of educational datasets.

## Project Background
The presence of PII in educational data is a significant barrier to the creation of open datasets. Automating PII detection reduces these risks and supports the development of tools and interventions for education.

## Dataset
The dataset consists of thousands of student essays from a massively open online course, processed to identify several PII categories such as names, emails, and phone numbers. Please note that some PII categories such as 'PHONE_NUM' and 'STREET_ADDRESS' have very low representation, presenting challenges in model training.

**Note:** The dataset exceeds GitHub's storage limit. It is recommended to run this notebook in a Kaggle environment for optimal performance and access to the dataset. The notebook can be accessed at the following link: 

[Optiver Model Comparison and Ensemble](https://www.kaggle.com/code/deeparker/pii-detection-with-deberta)

## Model Implementation
### DeBERTa for NER
We utilized the DeBERTa model, which has proven to be effective in various NLP tasks, including Named Entity Recognition. The model was fine-tuned specifically for detecting PII in educational texts. Custom loss metrics were employed to account for the severe data imbalance, prioritizing recall to ensure that sensitive data is not overlooked.

### Results
The model achieved high precision and recall across multiple PII categories. The F1-scores for different types of PII showcase the model's ability to understand and categorize sensitive information accurately. However, categories with fewer examples posed significant challenges in achieving reliable detection.

### Evaluation Metrics
We employed micro F1-score as our primary evaluation metric, emphasizing the balance between precision and recall. Also, custom loss functions were designed to better manage the imbalance by enhancing the model's sensitivity to less frequent categories.

## Challenges and Learnings
The severe imbalance in the representation of different PII types was the most challenging aspect of this project. Extensive pre-processing and the use of custom loss functions were required to address the imbalance effectively. The experience has underscored the importance of a robust training dataset and the effectiveness of transformer models in complex classification tasks.

## Conclusion and Future Work
The project underscores the potential of advanced NLP models in handling sensitive information. Future work will focus on expanding the dataset and improving the model's robustness against underrepresented forms of PII. 

## Acknowledgments
Special thanks to The Learning Agency Lab and Vanderbilt University for hosting this competition, providing resources, and supporting research in educational technologies.
