# <span style="font-variant:small-caps;">Project 4 - Exploring the NTSB Aviation Accident Database:</span>

#### <span style="font-variant:small-caps;">By: Ian Stack, Bruno Barreto, Robin Stopa</span>
---
## Executive Summary
### Contents:

-[Background](#Background)

-[Problem Statement](#Problem-Statement)

-[Description of Data](#Description-of-Data)

-[Conclusions and Recommendations](#Conclusions-and-Recomendations)

---
### <span style="font-variant:small-caps;">Background</span> 
The NTSB aviation accident database contains information from 1962 and later
about all the aviation accidents that happened around thw world. This data
includes both commerical and private airplanes.  Since the invention of the 
airplane, humans have made major advancenment on airplane safety in order
to make flying a very safe form of transportation.

Unfourtuantely, aviation accidents still occur all aroud the world. Recently,
on January 15, 2023, a commerical airplane went down in Nepal and there 
multiple fatalties(https://www.theguardian.com/world/2023/jan/16/nepal-plane-crash-facebook-live-video). Even with recent advacements, airplane safety and regulation
is important and needs to be constantly looked at.  This is why it is essential
to study the aviation accident data in order to reduce and furhter accidents.

In this notebok, I will be looking at the US aircraft accident data from 
[National Transporation Safety Board] (https://www.ntsb.gov/_layouts/ntsb.aviation/index.aspx) to help answer my problem statement

### <span style="font-variant:small-caps;">Problem Statement</span> 
The purpose of this project is to design a model for the plane safety regulators that can predict the severity of an aviation accident based on contextual factors and identify the most important factors as possible targets of regulation.

In this project our group will be utilizing both an NLP and linear regression model to predict the highest injury
severity based off other data in the database such as: make/model of plane, probable cause, and location.

### Goal
Our team will be able to predict the accident severity based other factors in the NTSB database

### Description of Data
#### Datasets
We want to explore this data set to learn more about the improvement of
aviation safety through the years. We download data from the **[NTSB
website](https://www.ntsb.gov/_layouts/ntsb.aviation/index.aspx)** . From this dataset we converted the database file from Mircosoft Access to CSV.  These altered dataset files can be seen in the data folder up above.

### <span style="font-variant:small-caps;">Data Dictionary</span>
|Feature|Type|Description|
|---|---|---|
|cm_probablecause|str|A column to describe the probable cause of the aircraft accident|
|analysis_narrative|str|Text that gives more detail on accident|
|cm_latitude|integer|latitude of where the accident occured|
|cm_longitude|integer|longitude of where the accident occured|
|cm_eventdate|str|contained the date of when the accident occured|
|cm_state|integer|the state in which the accident occured|
|make|str|A string of values that represent the make of the airplane|


### <span style="font-variant:small-caps;">Brief Analysis</span>
Our group started our analysis by looking over the dataset and seeing what factors would contrbute to helping us find out the severity of the accident.  From this point we bagan expolratory data analysis and looked for trends amonst the data.

### <span style="font-variant:small-caps;">Results</span>
|Training Accuracy|Testing Accuracy|Baseline|
|---|---|---|
|0.95|0.88|0.69|

### <span style="font-variant:small-caps;">Conclusions and Recommendations</span>
After our analysis on this dataset, we were able to look at different text and see how much more likely they are of a serious or fatal accident. Overall our model showed overfitting as the training accuracy was greater than our testing accuracy.  However, it did improve from the baseline.

For example 2 words that had feature importance in our model were the words: "Radar" and "Transmission".  A one word increase in the occurence of these words in flight narrative or probable cause was, 39,764 times for "Radar" and 86 times for "Transmission", more likely that the flight being seriour or fatal.  

Our results allow our team to look at the weight of certain words in aviation text and help us look at which words are connected to fatal or serious accidents.  This data can help aviation companies monitor flight text for certain key words that could indicate accident.

Recommendations:
Our team recommends to focus on training for maintence personnel with regards to installations in order to lessen the amount of aviation accidents.  Futhermore, expanding research on aircraft frames and innovate towards increased safety.








