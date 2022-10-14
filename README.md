# #WeRateDogs Twitters Data Wrangling
## by Olamide SHOGBAMU

### Introduction
This project is based on data wrangling. I use the #WeRateDogs twitter data archive for this project. The best practice of data wrangling was used in this project which is:

**Data Gathering**
I collected data from three different sources

  a. from a flat file [`twitter_archive_enhavced.csv`]()
  
  b. from a udacity database [`image_predictions.tsv`](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)
  
  c. from twitter API 

**Data Assessing**

The first two datab were pretty much ready for assessment, but the twitter API data was not because it was a in a JSON format. So, I prepared the twitter data for assessment by first dumping it JSON format file in a txt file which is then readable by pandas.

All the three data were accessed both visually and programatically and some quality and tidiness issues were spotted

**`Quality Issues`**

 - Column header (p1, p1_config, p1_dog, p2, p2_config, p2_dog, p3, p3_config, p3_dog) not descriptive enough.
 - Invalid data representation for percentage in p1_config, p2_config, p3_config
 - 745 None values as dog name
 - Some dog names are not feasibly correct like 'a', 'an'.
 - Text column contains url apart from the text column
 - Time stamp is contians string instead of date time format
 - Rating denominator can't be zero
 - Nondescriptive column header "id"

**`Tidiness issues`**

 - A single observation unit is stored in multiple column (doggo, floofer, pupper, puppo) shoild all be in dog stages.
 - Delete rows that are not original tweets


**Data Cleaning**
In this cleaning section, all the issues in the assessment were adrdresses and resolved using the Define-Code-Test approach. Some of the tools I used in the section are

- Pandas Dataframe rename column
- Pandas Column mapping and formating
- Pandas Split string into columns and drop columns
- Pandas merge
- Pandas to_datetime
- Pandas subseting a dataframe
- Adding columns together to make a string and manipulating the string



## Conclusion
At the end of the wrangling exercise, I created a visualisation to show the correlation between the favourite count and the retweet counts of tweets.

![correlation](https://user-images.githubusercontent.com/111246241/195943310-4ad4b825-df7e-47f7-9652-8860d1a2865c.png)

The correlation showed the comparism to be positive.

## Installation

This project requires [Jupyter Notebook](https://jupyter.org/) and [python 3](https://www.python.org/downloads/) to run.

Install the dependencies and libraries and start the server.

```sh
pandas as pd
numpy as np
matplotlib.pyplot as plt
seaborn as sns
```

