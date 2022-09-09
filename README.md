# pythondailycode
Python  Daily  Code

## Docs
- https://python.plainenglish.io/from-zero-to-hero-in-python-in-just-10-minutes-83064ffd5aee
- https://python.plainenglish.io/from-zero-to-hero-in-python-in-just-10-minutes-83064ffd5aee

## Install

```
pip install newsapi-python
```

##  Code 
````
from newsapi import NewsApiClient

# Init
newsapi = NewsApiClient(api_key='175b74679bc341e782cc4292c327c9ec')

# /v2/top-headlines
top_headlines = newsapi.get_top_headlines(q='bitcoin',
                                          sources='bbc-news,the-verge',
                                          category='business',
                                          language='en',
                                          country='us')

# /v2/everything
all_articles = newsapi.get_everything(q='bitcoin',
                                      sources='bbc-news,the-verge',
                                      domains='bbc.co.uk,techcrunch.com',
                                      from_param='2017-12-01',
                                      to='2017-12-12',
                                      language='en',
                                      sort_by='relevancy',
                                      page=2)

# /v2/top-headlines/sources
sources = newsapi.get_sources()
```
