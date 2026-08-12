# New York Post Gen Z Audience Analysis

This project came out of a collaboration between **St. John's University and the New York Post**. Our team was asked to look at how younger audiences consume news and think about ways the Post could improve its digital experience for Gen Z.

We surveyed St. John's students about where they get their news, what kind of content they prefer, when they consume it, what they like and dislike about existing news platforms, and what they would want from a news app.

Our team then used the survey findings to develop recommendations for the New York Post app and Project Hamilton.

## The analysis

The cleaned dataset has **546 responses and 80 variables**. I used Python to explore the survey data and look more closely at a few questions that stood out during the project.

Some of the main areas I looked at were:

- platforms students use to stay informed
- preferred news formats
- time of news consumption
- reasons for not using traditional news outlets more often
- features respondents would want in a news app
- whether short-form video preference could be predicted from demographic and behavioral information

The full analysis is in [`NY_Post_GenZ_Analysis.ipynb`](NY_Post_GenZ_Analysis.ipynb).

## A few things that stood out

Instagram and TikTok were by far the most commonly used social platforms for staying informed. Instagram was used by **85.2%** of respondents and TikTok by **66.8%**.

Short-form video also came through strongly in different parts of the survey. **43.8%** chose short-form video as their preferred news format, and **55.3%** selected short-form video stories or recaps as a feature they would want in a news app.

Another finding I found interesting was why respondents were not reading traditional news brands more often. **59.3% said social media already covers their news needs.** Time and format were also an issue for 39.0%, while 33.2% selected cost, paywalls, and advertising.

Personalization was another recurring theme. **50.2%** selected topic and local personalization as a feature they would value in a news app.

Taken together, these findings shaped a lot of our recommendations. Instead of expecting younger readers to change the way they already consume information, we looked at how the Post could fit more naturally into those habits.

## Testing the data a little further

I also wanted to see whether the survey data could tell us anything about **who prefers short-form news**.

I started with a logistic regression using age, gender, consumption frequency, and time of consumption.

The result wasn't particularly strong:

| | Accuracy | Baseline |
|---|---:|---:|
| Model 1 | 56.5% | 55.6% |

The model was barely better than simply predicting the majority class.

I then added behavioral information such as platform usage, engagement style, and social-media behavior.

| | Accuracy | Baseline |
|---|---:|---:|
| Model 2 | 65.4% | 56.1% |

That was a much more noticeable improvement.

TikTok usage also had a positive association with short-form video preference in the fitted model.

For me, the useful takeaway wasn't just that the second model had higher accuracy. It was that **behavior told us more than demographics alone**. Knowing how someone interacts with news and digital platforms was more useful in this sample than simply knowing their age or gender.

The model is exploratory, so I wouldn't treat it as a recommendation engine or make causal claims from it.

## What we recommended

Based on the survey, app review, and our broader project work, our recommendations focused on:

- making short-form video and quick recaps easier to find
- giving readers more control over topics and local content
- using personalization rather than giving every reader the same experience
- improving the path from social-media discovery to the NY Post app
- making notifications more relevant to individual users
- reducing friction from ads, paywalls, and the overall mobile experience
- using Project Hamilton as an opportunity to build a more personalized news experience

One question we kept coming back to was how to make the product more appealing to younger readers **without alienating the Post's existing audience**.

Personalization gave us a way to think about that. The product doesn't necessarily need to look or behave the same way for everyone. A younger reader could have a more visual, personalized experience while another reader could continue using a more traditional version of the Post.

## Tools

`Python` `Pandas` `NumPy` `Matplotlib` `Scikit-learn` `Google Colab`

The notebook includes data cleaning, exploratory analysis, visualizations, logistic regression, train/test evaluation, baseline comparison, and coefficient interpretation.

## Files

- `NY_Post_GenZ_Analysis.ipynb` — Python analysis and modeling
- `cleanedsurveydata.csv` — cleaned survey data used in the notebook
- `Executive_Summary.pdf` — summary of the project and findings
- `App_Narrative.pdf` — our app review and supporting recommendations
- `Fourmidables_NY_Post_Presentation.pdf` — final team presentation

## Authors

This project was completed by **The Fourmidables**:

**Anthony Pepe**  
**Antonio Castillo**  
**Shalini Chhetri**  
**Isabela Urena**

St. John's University  
Peter J. Tobin College of Business

## Note on the data

The survey was conducted primarily with St. John's University students, so the results shouldn't be read as representative of Gen Z as a whole.

The survey is also self-reported. The modeling in this repository shows relationships within this sample, not cause-and-effect relationships.

## Usage

This repository is public so I can share the project as part of my professional portfolio.

Please do not copy, reproduce, redistribute, or use the dataset, analysis, presentation, written materials, or recommendations for commercial purposes without permission from the appropriate authors or rights holders.

If you reference the project for academic or educational purposes, please credit the project team.

New York Post names, logos, trademarks, and other third-party materials belong to their respective owners.

**© The Fourmidables. All rights reserved.**
