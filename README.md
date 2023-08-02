# Text-Processing-with-NLTK
    #NLTK     #NaturalLanguageProcessing     #TextProcessing     #Tokenization     #StopwordRemoval     #Stemming     #Python     #TextAnalysis     #TextMining     #DataPreprocessing     #TextData     #NLP     #DataScience     #DataCleaning     #MachineLearning     #CodeExamples     #TextProcessingLibrary     #DataManipulation    


import nltk
from nltk.corpus import stopwords
from nltk.tokenize import sent_tokenize, word_tokenize

text = """Muad'Dib learned rapidly because his first training was in how to learn.
And the first lesson of all was the basic trust that he could learn.
It's shocking to find how many people do not believe they can learn,
and how many more believe learning to be difficult."""

text = text.lower()

stop_words = set(stopwords.words("english"))
filtered_list = []

words = word_tokenize(text)  # Tokenize the text into words

for word in words:
    if word.casefold() not in stop_words:
        filtered_list.append(word)

print(filtered_list)
