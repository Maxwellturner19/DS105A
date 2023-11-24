<font style='font-size:3em'>**📝 Analysis of US Presidential Elections 1944-2024** </font>

**PURPOSE**: This is a submission for the DS105 Week07 Summative assignment with a purpose of scraping data from **multiple WIKIMEDIA projects** to create an overview and greater understanding of the US Presidneital Elections since the Second World War.

<a href="https://en.wikipedia.org/w/index.php?title=Special:Search&limit=56201&offset=0&ns0=1&search=United+States+presidential+election">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b3/Wikipedia-logo-v2-en.svg/300px-Wikipedia-logo-v2-en.svg.png" alt="Wikipedia" width="10%">
</a>

**LAST REVISION:** *16th November 2023*

**Hypothesis:** I began by creating a hypothsis that higher voter turnout should result in lower winning margins, for the dominant two parties in the US Presidential elections. 

**Citation:** Jones, M.I., Sirianni, A.D. & Fu, F. Polarization, abstention, and the median voter theorem. Humanit Soc Sci Commun 9, 43 (2022). https://doi.org/10.1057/s41599-022-01056-0

This is based of a theory in political science which states that 
This is based on a theory in political science which states that: 
 - **a.** Higher voter turnout suggests people care more about this election compared to others. 
 - **b.** People tend to care about elections more when they are polarizing.
 - **c.** A polarizing election means the nation is highly split and there is no clear winner coming into voting day.
 - **d.** Therefore, more people will be more likely to vote for one of the two possible candidates to ensure their choice is counted.
 - **e.** A higher turnout for the main two candidates should therefore mean a lower winning margin as there is little evidence coming into the election of a clear winner, and the election is polarizing.


**What I did:** 

1. I scraped data from wikipedia to create a dataframe of the links + Titles of the pages I wanted to scrape.
2. I used this dataframe to extract data from tables within these links.
3. I extracted the relevent data I wanted from the "Results Table" to test my hypothesis.
4. I put this into a dataframe and use this to conduct analysis.
5. I plotted Electoral votes over time and popular voter margin.
6. I ran a regression analysis of popular vote margin and total popular votes for both parties.
7. I concluded that there is no statisstical significance or correlation.
8. I used a second wikiproject and scraped data from WIKINEWS on all news stories of presidential elections
9. I created a dataframe with the links and news headings for these news stories
10. I created a wordle for each collection of election news articles available on Wikinews.
11. I used the NLTK to analyse polarity scores of the article texts to compliment my hypothesis.
12. I out these polarity scores into a **merged** dataframe with the election table data extratced in NB02
13. I wrote conclusions of my analysis and findings.

**My Findings:**
- I consluded that there is no significant relationship between turnout (total popular votes) and winning vote margins (popular vote margin).
- WikiNews is a reletively neutral news soruce which mostly repsots facts and uses little emotive langauage or bias in its articles, therefore it is difficult to assess the palarity of elections with this data alone.
**my conclusions can primarily be found within their respective NBs**

**Where is everything?**

- NB01 = This Jupyter Notebook contains the scraping of the page titles and links for the Wikipedia pages with the US presidential Elections from 1944-2024. I create a dataframe with this information called *Elections.cvs* in /Data folder.
- NB02 = This Jupyter Notebook contains the data scraped from tables within the 21 links established in NB01 in a dataframe. It also has the analysis I have completed with this data to test my hypothesis.
- this analysis is within the /Analysis foldeer and has visualisations of popular vote margins and winning vs loosing electoral votes from 1944-2020
- this folder also contains the linear regression of popular vote margin and total popular votes
- NB03 = This Jupyter Notebook contains scraping of wikinews articles on the elections from 2008-2020. There is also some analysis of the content of these articles. 
- I merge the polarity dataframe with the elections results dataframe at the end of this NB.

**What you need to download for this project:**

- import pandas as pd
- import requests
- from scrapy import Selector
- import nltk
- from nltk.corpus import stopwords
- from wordcloud import WordCloud
- import matplotlib.pyplot as plt
- from textblob import TextBlob
- import seaborn as sns



**Use of Generative AI assistants:**
- I often used github copilot to finish funtions off and correct sytax.
- I also used #instruction to prompt code to give me insight of how to format a funtion/list comprehension 
- I restricted the use of ChatGPT to sid my learning of new concepts. this made the task a lot more timely than perhaps would have been with ChatGPT assistant.
- I still used it sometimes for idea generation for analysis pointers as this is not something I could use lecture/lab notes for. 