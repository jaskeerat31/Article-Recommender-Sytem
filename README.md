In this project we will apply Collaborative Filtering, Content-Based Filtering and Hybrid methods in Python, for the task of providing personalized recommendations to the users. The dataset we use here is taken from KAGGLE https://www.kaggle.com/gspmoreira/articles-sharing-reading-from-cit-deskdrop 

Basically what we are doing is that we are recommending articles to users based on their preference and activity on the platform.
Description of Data:
shared_articles.csv
Contains information about the articles shared in the platform. Each article has its sharing date (timestamp), the original url, title, content in plain text, the article' lang (Portuguese: pt or English: en) and information about the user who shared the article (author).

There are two possible event types at a given timestamp:

CONTENT SHARED: The article was shared in the platform and is available for users.
CONTENT REMOVED: The article was removed from the platform and not available for further recommendation.
For the sake of simplicity, we only consider here the "CONTENT SHARED" event type, assuming (naively) that all articles were available during the whole one year period. For a more precise evaluation (and higher accuracy), only articles that were available at a given time should be recommended, but we let this exercice for you.

users_interactions.csv
Contains logs of user interactions on shared articles. It can be joined to articles_shared.csv by contentId column.

The eventType values are:

VIEW: The user has opened the article.
LIKE: The user has liked the article.
COMMENT CREATED: The user created a comment in the article.
FOLLOW: The user chose to be notified on any new comment in the article.
BOOKMARK: The user has bookmarked the article for easy return in the future.

In this project, we've explored and compared the main Recommender Systems techniques on CI&T Deskdrop dataset. It could be observed that for articles recommendation, content-based filtering and a hybrid method performed better than Collaborative Filtering alone.

Assumption
In this example, we've completely ignored the time, considering that all articles were available to be recommended to users at any time. A better approach would be to filter only articles that were available for users at a given time.
