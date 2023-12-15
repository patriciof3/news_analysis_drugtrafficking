# news_analysis_drugtrafficking
This is a series of notebook implemented to perform text analysis of news regarding drug trafficking from two different newspapers. It includes code for  capturing results from google search,  scrap those links to extract date and content of the articles, and finnaly perform topic modeling to analyse the media coverage. 

The file "scrapping_google_search.ipynb" contains code for performing a scrapping of a media outlet (ellitoral.com) fron Santa Fe, Argentina. I used the free versión of the zenserp API to retrieve the links for results of an google query. Then, with the Beautiful Soup library I provide a script to identify for this particular website the html tags related to the date, title, and subtitle of the articles.

Having assembled a dataframe with these results I preprocess the content of the articles to prepare ir for a topic modeling. With "spacy", stopwords are eliminated and lemmatization achieved. Then I use CountVectorizer from sklearn to vectorize the content and finally I use the component LatentDirichletAllocation from sklearn.decomposition to perform the topic modeling.

In this repository I also uploaded two html files containing the results from the topic modeling plotted by the library pyLDAvis. The two files correspond to two different media oulets (ellitoral; ellitoral.com / p12; pagina12.com.ar), and are interesting to visualize how the media coverage focused on different aspects of drug trafficking.
