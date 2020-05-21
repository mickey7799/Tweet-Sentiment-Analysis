# Tweet Sentiment Analysis


Use machine learning methods to categorize short messages (“tweets”) from Twitter to analyze the writer’s attitude (positive, negative or neutral) towards a particular topic.

## Data
- Raw text of 22,987 tweets for training
- 4,926 for evaluating
- 4,926 for testing

## Data Processing 
- Tokenized the raw tweets data
- Get rid of stop-words, symbols, and urls
- Stemming
- Kept the name tags because I assumed that mentioning some famous people such as Trump may link to certain emotions
- Use TF-IDF as the value of each attribute (which takes into account both term frequency, rareness of the term, and the length of tweets.) 
- 34,641 attributes

## Models 

### Baseline Model
It is created by always outputting “neutral” result because there are about half neutral-tagged training data. 

### Naive Bayes
As a simple and scalable model, Naive Bayes works well on text categorization. 

It analyses each feature independently, so it made use of all tokens in feature vector but it cannot deal with combination of tokens, which might be meaningful for text sentiment.

### Random Forests
Random Forests is a rule based classifier, it can take into account the combination of tokens. For example, the combination of “Great” and “Job” might be a positive tweet.

## Future Improvements
- Optimization of the attributes selected using feature selection to derive features contributing most to the sentiment classification to avoid having irrelevant features in the dataset, which would decrease the accuracy of the models because model would learn based on irrelevant features.
- Creating more attributes by using n-gram, POS, or counting of transformed words such as elongated or all-caps words.
- Giving different weights to terms such as for terms that are more related to sentiments, the weight of those term values is increased for better prediction.   
