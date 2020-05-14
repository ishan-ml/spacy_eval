# Outcomes and methods

## Datasets Used :

1. Enron emails (https://www.cs.cmu.edu/~enron)
2. OntoNotes 5.0

## Evaluation metrics used:

1. Accuracy score
2. ROC
3. F1 score
4. Confusion matrix

## Progress so far

I annotated the OntoNotes dataset using spacy NER, then treating the pre-annotations in the dataset as labels for performance and accuracy evaluation.
Since we have to focus on only organization labelling, I divided the labels into 3 categories -1,0,1
where -1 means spacey didn’t  give any entity name to the sentence,0 where the entity label was not ORG and 1 where entity was ORG respectively.

1. Accuracy score :  0.9676

2. Evaluating the OntoNotes dataset I found out F1 score for 3 categories of data as follows :
[0.        , 0.98101418, 0.91691935]

Score of -1 is 0 since pre-annotated data had no -1 labels.

3. Confusion matrix evaluated as follows:

class -1:     [   0,    0,    0],
class  0:     [  25, 4082,   98],
class  1:     [   4,   35,  756]

So in total misclassified 'ORG' labels are 39.

4.ROC : 

fpr : [0.        , 0.02330559, 0.9940547 , 1.        ]

tpr : [0.        , 0.9509434 , 0.99496855, 1.        ]


**Currently simplified enron data in readable dataframe **

## To do

Further simplification of enron dataset is needed to properly evaluate spacy's performance on it


## Conclusions so far

1. Also by observing the 'ORG' labels which were not classified by spacy the issue can be solved by removing punctuations from sentences or specifing some peculiar organisation name(ex.The Truth Squad).

2. The documentaion of organization  can be improved by adding some research institutes and scientific publications such as Astrobiology Journal.

3.Some of the errors made were due to I  missing context.




