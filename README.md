**Text-as-Data Coursework**

It focuses on implementing and evaluating a multiple-choice question-answering system using various text processing and machine learning techniques.

**Dataset**

The dataset is derived from the WikiQA corpus and consists of training, validation, and test splits. The dataset contains:

* Questions

* Four possible answer choices per question

* A labeled correct answer

**Tasks and Implementation**

1. Dataset Preprocessing

Objective: Tokenize and explore the dataset.

Implementation:

* Tokenize text using text_pipeline_spacy_special.

* Compute statistics (e.g., average token count per question and answer choice).

* Perform exploratory data analysis.


2. Set Similarity Measures

Objective: Use set-based similarity measures to find the best-matching answer.

Implementation:

* Compute overlap coefficient, Sørensen-Dice, and Jaccard similarity.

* Evaluate accuracy on training and validation sets.

* Handle cases of tied similarity scores.


3. Cosine Similarity with Term Frequency Vectors

Objective: Use TF-based cosine similarity to select answers.

Implementation:

* Convert text into term frequency vectors using CountVectorizer.

* Compute cosine similarity between questions and answer choices.

4. Cosine Similarity with BERT Embeddings

Objective: Use contextual embeddings from bert-base-uncased.

Implementation:

* Extract [CLS] token embeddings.

* Compute cosine similarity for answer selection.

5. Fine-Tuning BERT for Answer Selection

Objective: Train a transformer model for classification.

Implementation:

* Format data for AutoModelForSequenceClassification.

* Trained using pre-defined hyperparameters.

