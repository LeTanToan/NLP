# CAPP30122-Project-
CAPP30122 2018 Group Project By WXD

Data downloaded from https://www.kaggle.com/hugodarwood/epirecipes/data

## Scripts in our project:

In the cookbook folder:

1.	Vector_space.py, a python file containing data preprocessing and vector space model construction
2.	BM25.py, a python file containing data preprocessing and probabilistic BM-25 model construction
3.	Scrapeimage.py, a python file scraping image from google

Note: data preprocessing has already been added to Vector_space.py and BM25.py

In the evaluation folder:

1. project.py, a python file that evaluates vector space model and BM25 model based on normalized discounted cumulative gain score.

## Files in our project:

### In the cookbook folder

for Vector_space.py and BM25.py, the documents are originally generated by our save_func function. We delete the save_func steps and directly load the following documents to shorten running time.

1.	For Vector_space.py, doc_length, documents, index_in_json, inverted_index, word_set are saved
2.	For BM25.py, doc_length_BM25, documents_BM25, index_in_json_BM25, inverted_index_BM25, word_set_BM25 are saved

### In the evaluation folder

1. The following documents are also generated by the save_func function.

doc_length_BM25_removed_stop_words, doc_length_tfdf_removed_stop_words, documents_BM25_removed_stop_words, 
documents_tfdf_removed_stop_words, index_in_json_BM25_removed_stop_words, index_in_json_tfidf_removed_stop_words,
inverted_index_BM25_removed_stop_words, inverted_index_tfidf_removed_stop_words, word_set_BM25_removed_stop_words,
word_set_tfidf_removed_stop_words

2. evaluation.xlsx includes our results for evaluation



## To run the project:

1.  Install pip in your terminal (if have not done so)
2.  To run the project using Django user interface: $ pip install Django
3.  Go to “cookbook” folder, run: $ python3 manage.py runserver
4.  Go to 127.0.0.1:8000/search/
5.  If you want to use a different model, go to views.py in cookbook/search/views.py, change "from BM25 import * " to "from Vector_space import * "


## To run model evaluation:
1.  Please change the directory into "evaluation" folder.
2.  Run python project.py.
3.  You can see the scoring process shown in the terminal and it will print the score for ten queries we selected for both TFIDF model and BM25 model.
4. Please open the evaluation.xlsx file to see the histogram for comparing NDCG value for two models.

## Responsibilities:

1.	Data Preprocessing: Wenxi Xiao 
2.	Build models and algorithms: Lerong Wang, Wenxi Xiao, Yangyang Dai
3.	Django user interface: Lerong Wang, Yangyang Dai
4.  Model Evaluation: Wenxi Xiao

## Documentation of Code Ownership:

1. "Direct copy"  ~ Learned from online sources, Generated by installed package (Django or other) and few edits made               
2. "Modified"     ~ Generated by installed package (Django or other) and meaningful edits made  OR  heavily utilized template(s) provided by tutorial sessions (TA- or Django-generated)                                     
3. "Original"     ~ Original code or heavily modified given structure       
