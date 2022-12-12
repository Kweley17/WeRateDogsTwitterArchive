# Data Wrangling efforts
The provided datasets were `twitter_archive_enhanced.csv`, `image_predictions.tsv` and 
the `tweet_jspn.txt`. A quick summary of the quality issues identified and solved are as follows: 
rating_denominator values were differing as opposed to all being 10
innacurately extracted names for dogs
`timestamp` column was of string dtype instead of DateTime
unnecessary tweet data like retweets
null values in columns among many more 

# Tidiness issue 
Multiple variables referring to one variable (`dog_stage`) 
I resorted to melting these into one variable, then dropped the resulting duplicate variables
I used left merge to join the datasets on their shared variables to form the master dataset `twitter_archive_master.csv`