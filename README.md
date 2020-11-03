# 🌟NLP-on-10K-Documents(Financial Documents)🌟

📄Scraping and Analysing Financial Documents filled by Publically Traded Companies📄

🏢Publicly traded companies in the United States are required by law to file reports with the Securities and Exchange Commission (SEC) on "10-K" and "10-Q." These reports include qualitative as well as quantitative explanations of the success of the business, from sales estimates to qualitative risk factors. "Companies are required to disclose" important pending litigation or other legal proceedings "details. As such, 10-Ks and 10-Qs also provide useful insights into the success of a company. As such, 10-Ks and 10-Qs often hold valuable insights into a company's performance.


### Methodology

1. Scrape the 10-K documents from the SEC EDGAR Database for a set of publicly traded firms. Upon scraping, we perform some basic data-cleaning and pre-processing for the 10-K document (removing HTML Tags and numerical tables, converting to txt files, lemmatisation, stemming, removing stop words, and so on).
2. After pre-processing we analyse the textual data from one of the 10-K documents using Exploratory Data Analysis(EDA) techniques such as Bag of Words(BoW), TF_IDF, Wordcloud, LDA modeling with interactive pyLDAvis, Top 20 most frequently used words, and Positivity score of the 10-K document using Textblob library.
3. For a particular company, we calculate the cosine similarity and the Jaccard similarity over the set of 10-Ks that were scraped(cosine and Jaccard similarity are relatively less computationally intensive to compute). We calculate the similarity by comparing each 10-K document with the previous year's 10-K and given it a score. We then calculate the difference between these similarity scores and compare this over the years.
4. Try to map these text changes with the stock price movement for the firm. We download the prices of the stock from the first-time the 10-K document was available till the day the lasted 10-K document was filed. Upon carefully analysing, we can conclude as to whether the results align with the hypothesis or not.

<br/>
