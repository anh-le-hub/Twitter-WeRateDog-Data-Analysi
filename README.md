# Twitter-WeRateDog-Data-Analysis
This project wrangles the Archive Data collected about WeRateDogs tweets in 2017 to look for interesting insights. 

## The Data
Are stored in "Data" Branch
1) Enhanced Twitter Archive, i.e. twitter_archive_enhanced.csv: The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets

2) Additional Data via the Twitter API, i.e. tweet_json.txt:  Back to the basic-ness of Twitter archives: 
retweet count and favorite count are two of the notable column omissions. This additional data can be gathered by anyone 
from Twitter's API. Using the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this data 
for all 5000+. This was done via query Twitter's API.

3) Image Predictions File, i.e. image_predictions.tsv: file downloaded programmatically from Udacity website, containing the 
prediction of the dog breed in each tweet
- tweet_id is the last part of the tweet URL after "status/" → https://twitter.com/dog_rates/status/889531135344209921
- p1 is the algorithm's #1 prediction for the image in the tweet → golden retriever
- p1_conf is how confident the algorithm is in its #1 prediction → 95%
- p1_dog is whether or not the #1 prediction is a breed of dog → TRUE
- p2 is the algorithm's second most likely prediction → Labrador retriever
- p2_conf is how confident the algorithm is in its #2 prediction → 1%
- p2_dog is whether or not the #2 prediction is a breed of dog → TRUE
etc.

==> The cleaned data are combined & stored in twitter_archive_master.csv
