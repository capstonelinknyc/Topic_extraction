# Topic_extraction

## Text data

Intersection Co. provided a list of URLs of news articles. We scraped the text data from websites using a built-in Beautiful Soup Python library and proceeded to preprocessing. As text data from different articles contain the same words but vary in case (capitalized, non-capitalized, all caps), we converted all letters to lowercase. We also removed numbers, punctuation marks, whitespaces in the text content as they may appear in the model output without adding any meaning. We removed stop-words such as “I” “and” and “the” since these words are so common that they tend to be over-represented in the results. The dictionary of stop-words was borrowed from stopwords module in Natural Language Toolkit (NLTK) open source Python library. 


## Latent Dirichlet allocation (LDA) model 

Latent Dirichlet allocation model (LDA) is a textual analysis method used to understand the most important terms in a text.  Before applying LDA model text data needed to be preprocessed, like  using the Inverse Document Frequency (IDF) which refers to the inverse fraction of documents in the words collection which has specific term. The more this term appears, the lower the IDF score is. In this way, they get IDF score for words and by sorted them, stop words can be collected.  The number of topics as K in LDA model which is modifiable, to cluster articles into K types. After brief experimentation, we settled on K = 6 due since it gave us both a good amount of keywords and is easy to interpret.

LDA lets sets of observations to be explained by unobserved groups that explain why some parts of the data are similar. If these observations are words that are collected into text files, it posits that each text file is a mixture of a small number of topics and that each word's presence is attributable to one of the document's topics. As mentioned before, we use this model to determine the important keywords in articles about LinkNYC and broadband access. 

## How do top topics of LinkNYC change by years?

With the articles provided by LinkNYC we built topic models included 6 topics and each of them had 5 top terms. The top terms for 2018 can be found in Table X, while terms from other years can be found in Section x.x. of the Additional Materials.

In 2015, top terms included  “access”, “phone”, “free”, “best”, “wifi” and “news”. Right after LinkNYC emerged, media focused more on introducing LinkNYC and studying about services that LinkNYC can provide. 

In 2016, top terms were consisted of words like “digital”, “display” and  “business”. At this point, media started responding to the commercial nature of LinkNYC. Advertisement displayed on their devices played an important role in marketing and spreading ideas. 

In 2017, the top terms changed to “data” , “company”, “public” and “technology”. After years of data collection and accumulation, media started showing interest in data collected by LinkNYC. 

In 2018, top terms didn’t seem to change much which still included “data”, “public” and “information”. The interest to data was growing under the development of artificial intelligence.


