# Fake-and-Real-News
The main objective was to predict whether a news article is Real or Fake, given their **title** and/or body of **text**.<br>

The dataset was acquired from kaggle, and contained news predominantly from the years 2016 and 2017.<br> After cleaning and wrangling, fours features were carried forward to be used in modeling: title, text, title-length, and text-length. The latter was eventually dropped after statistical analysis (non-distinguishing feature among real and fake data).<br>

EDA revealed certain words (e.g. Trump, President) to be found in *both* real and fake news, while others were more prevalent in real (e.g reuters, Washington, state) or fake(e.g. hilary, donald, obama) news. Additionally, fake news titles were *longer* with higher word counts.<br>
It is interesting to note that in 2016 (an election year), there were double the number of fake news articles than real news. While 2017 had double the amount of overall news, it had 2.5 times *less* fake news than real.<br>

Among the three models compared (Naive Bayes, Logistic Regression and PassiveAgressive) Naive Bayes was the fastest performing (3 to 4 times faster than the others). Even though it had a low accuracy in the 'test' data, it had superior prediction when using a 'blind' test set.<br>
A final big leap in model improvement was the result of dropping all non-alphabetic characters from the text of the article, and modeling with Naive Bayes. The final **blind test accuracy was 70%**.

This repository contains reports, code and slides pertaining to this project.
- **Milestone Report** is a jupyter notebook with code, and documentation on data wrangling and EDA (exploratory data analysis).
- **Statistical Analysis** is a summary of simple statistics on the original and engineered data.
- **Machine Learning and Analysis** is the bulk of the work with various ML hyper-parameter and model tests. Improvements were a learning process which culminated in a 10% jump in overall f1 increase, and a marked improvement (40% f1 increase) in the fake news prediction.
- **Slides** is a summary presentation of the project.<br>

