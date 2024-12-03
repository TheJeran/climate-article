## Overview
These datasets are saved in pickle format. Use [pandas.read_pickle()](https://pandas.pydata.org/docs/reference/api/pandas.read_pickle.html) for easy loading. 

#### first_response.pkl
This is the raw unfilitered input data from the website (minus the IP information)

#### delayed_response.pkl
This is the raw unfiltered input data from the website after one week (minus the IP information)

#### survey.pkl
This is the survey responses

### Cleaned Data
#### article_goodfaith.pkl
This is the article data from <i>first_response.pkl</i> after having the good faith filter applied to it. 

#### video_goodfaith.pkl
This is the video data from <i>first_response.pkl</i> after having the good faith filter applied to it. 

#### New columns
Both of the above datasets also have additional columns added to them

* **correct** The correct responses in the quiz. Calculated from _mc_#_ and _tf_#_ columns
* **article/video_time** The time in seconds the user spent on the format calculated from _formatStart_ and _formatEnd_ columns
* **media_pref** User media prefernce. Obtained by subtracting _pref_1_ from _pref_0_ 

