# Auto-correction-for-transliterated-queries
### This is a query correction system that is designed for transliterated queries. This project is a part of the transaction paper *Auto Correction and Sense Disambiguation in Transliterated Queries*, which is currently under review.  
### Key features of the model:
  - Can be retrained on a new data-set of well spelled queries in mixed languages such as Hindi-English, English-French, Hindi-Bengali, etc.
  - No need of annotated data-set, only need well spelled dataset.
  - Can be trained on smaller dataset - ~10K queries, giving reasonable performance. 
  - A trained mocdel on English corpus is provided, queries are taken from Yahoo webscope - 150K questions. 
  
### Usage:
```python
obj = auto_correct()
obj.run()

enter a query
hw to lrn pythn anddeeplearning eas ily
how to learn python and deep learning easily    11.2134873867
```
### Parameters of the model
There are two parameters of the auto-corrector:
```python
obj = auto_correct(retrain=,data=)
```
For retraining the model, set `retrain` = `True` and pass the queries as the other argument. The queries must be given in the following format:
```python
queries=[]
queries = ['how to handle a 1.5 year old when hitting',
 'how can i avoid getting sick in china',
 'how do male penguins survive without eating for four months',
 'how do i remove candle wax from a polar fleece jacket',
 'how do i find an out of print book']

obj = auto_correct(retrain=True,data=queries)
```
