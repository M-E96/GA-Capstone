# Capstone - Climate Change, CO2 Impact and Proportionate Input for Effec

## Introduction

The Aim of this capstone was to find out just how much CO2 actually had an impact on Climate Change, or at least what we believe to be the results of climate change, such as rising global temperature; which is the main focus. We then modelled to predict/future forecast, to prove that CO2 influences global temperature, as well as as seeing if the COP worries and predictions were valid. We would use a mixture of ARIMA, VAR and RNN modelling in this pursuit. We will use these models to not only future forecast to see if the COP predictions are accurate, but if RNN VAR are more accurate with more variables, it proves that CO2 influences temperatures, and these 2 plus sea levels influence disasters. Finally, we would then see just how much of this effect, if proven to lead to disaster, is proportionally being felt by those who contribute most towards it.

### Data Dictionary

|Feature|Type/s|Dataset|Description|
|---|---|---|---|
|**Year**|Float/Int|All Datasets|Year at which data was taken|
|**Entity/country/country name**|Object|All Datasets|The name of the country from which we are measuring the data from|
|**Disasters**|Int/Float|natural-disasters|Frequency of disasters per year|
|**Black Carbon Emissions**|Int/Float|air-pollution|Amount of black carbon particulate produced by a nation|
|**Temperature anomaly/variants**|float|temperature-anomaly|change in temperatre relative to average in 1961-1990|
|**Annual CO2 emissions/And variants**|int/float|annual-co2-emissions-per-country|Amount of CO2 emissions per nation/region/collective|
|**Average sea level**|Float/Int|sea-level|Average sea level of both Church and White(2011) and UHSLC|
|**Average Surface temperature//1**|Float/Int|average-monthly-surface-temperature|Min and Max temperature of monthly data of each country|
|---|---|---|---|
|*Units mentioned*|
|temperature anomaly|Float/Integer|Celsius, relative to average in 1961-1990|
|CO2 emissions|Float/Integer|Tonnes of CO2
|BCE|Float/Int|Tonnes of Black Carbone Particulates|
|Average sea level|Float/Int|mm relative to average of 1993-2008|
|Average surface temperature/.1|Float/Int|Degrees Celsius|
|Disasters/variants|Int|Frequency of Disasters|

## Executive Summary
> When people talk about climate change, the initial thought is to our fossil fuel consumption and CO2 emissions. But we explore why using CO2 as a measure of human impact is valid, and why scientists have been focused on it for so long. 

>Whilst there are other contributors to Global warming, much more potent, CO2 is actually the most humans actually have an impact on.

> CO2 emissions, sea levels, global temperature, average surface temperatures, number of disasters all increase, just by pure eda, and through ARIMA, VAR modelling. These all either contribute or are a product of Global warming, but to be honest, mostly likely both, a vicious cycle.
>> But, as opposed to just generally increasing, we sea that in all these data points, the sharpest rates of increase all span from the 1960s to 2000, which can be attributed to the normalisation(it being post war) and industrialisation for China, India, Russia.

> ARIMA is good for single series data, just to make simple predictions, VAR for interdepencies, multiple variables, predictions should be more accurate if our hypothesis is correct about CO2, temperature, Sea level are all related, thus producing more disasters.
>> Time was used to do individual modelling, but when you introduce more variables, it becomes inherent, as long as you keep the sequence of it the same, since they are cast to the same dataframe, and index, which is what we would have set as our time. This is also true for RNN, as long as we did not shuffle our data. The index being time wasn't a necessity, but just being ordered was.

> During our ARIMA modelling, we noticed that the trends were too small to capture over such a huge span of time, including there being notable wars and economic depressions up until the 60, and we see a massive improvement in prediction if we start from that metric, which we ended up doing. We also noticed in our decomp,eda,pacf/acf, that these environmental data points were ideal for ARIMA, hit all the metrics, perhaps signalling that our data was too simple.

> Made separate notebook for RNN as ran on Collab. Does show CO2 impacts on global temperature, may seem small but the changes we are looking for/COP is aiming for is tiny.
Disasters was less successful, but given the trend in the graph, it seems understandable, and actually seems quite accurate, although not reliable, for the anomalous figures. Although clear there still is an increase.

> VAR was used to show that relatively, CO2 is tied into global temperatures, and that all the variables I used, sea level, CO2 emissions, and global temps "cause" the increase of natural disasters.

> Showing proportion of input into total global emissions, then seeing which nations input the most, and the ones suffering the most from the effects of climate change.

## Conclusions

Whist I can say I have somehow shown that COP was right about the current projections for sea levels, temperatures and the consequences(Disasters) through use of the models, as well as CO2 emission's influence on climate change, through use correlation to global rising temperatures; How confident I can say I am in the models are another question. Whilst I may have seemed to show that we reach 1.5C before 2050 and with no trend to stop, the nature of the dataset, as well as the nature of the type of data(Environmental) proved either to be too complex in nature, the latter, or too simple of a dataset to encampsulate the true interdependency between my chosen variables and the patterns they exhibit themselves. I believe, that whilst I can definitely gather more data, the methods I used are probably too simplistic as well, chaos theory I believe embroils environmental data, but I do not believe that it is impossible to produce a reliable/confident model and future forecast; for despite what I have said, I have done it to some extent, keeping with the prediction. Whilst not the best, the one thing for sure that remains is that a pattern and trend clearly exist, just to what extent they are increasing, interdependent and affecting climate change is a confidence level I would like to improve on the future.

## Considerations
- I definitely could have included more of my work in the notebook in the slides, better explanations of the models and why I went forward with them, or at least go through the time series model behaviours.
- I should have done a correlation or proporion equation for KYOTO and CO2, would have been more informative and impactful
 - Whilst there was a clear aim within this project, I believe the peripheral eda and statements, such as the players, proportionate and disproportionate effects/impacts was either incomplete or hard to tie in. It seems I was either trying to fit in too much, or planning a presentation that spans much longer. Must definitely repurpose this project and either expand or reduce, a lot of unsubstantiated points I believe. I feel I lack the explanation in the slides, would love to go into more detail.
 - Hypothetical modelling would have been a good touch, inputting ideal situations, so that we can see if the effects subside or not, and just more modelling based on other variables.
 - More modelling in general, to contrast my predictions would have been nice as well, as well as other ways of future forecasting.
 - Although I have already mentioned, perhaps more eda on the players section, and done some direct calculation on the proportions and effects, some figures to show would have been better. Not too hard to calculate either.
- Delving into renewables would have been relevant and adds information on the side of the Players EDA, tie it into change in CO2 emissions, as well as the import export to see how much greenwashing actually has an effect, that perhaps it's not as serious as people convey. As well as other greenwashing techniques. As well as individual disasters, see if I could find correlation with the variables most obviously correlated, sea level for drought, temp for extreme temperatures etc... Too general in disasters. More diversity in disasters.
- Find out why RNN failed for sequence length greater than 1. 
- Should have done a country correlation calculation for input and output, as well.
- Same problem with the section regarding BCE, not enough data, or explanation in the slides. Make message clearer and substantiate, Use Sneaky scraping technique to get the data.
- To add onto hypothetical modelling, what if wars/depressions hadn't occurred, how much worse would it have been? As well as considering renewables, just how much would we need to have adopted to make up for CO2, as renewable manufacturing also incurs CO2 emissions currently. Most electric power is fossil fuel powered.

 
### Sources
- https://ourworldindata.org/co2-and-greenhouse-gas-emissions?insight=human-greenhouse-gas-emissions-have-increased-global-average-temperatures#key-insights
- https://ourworldindata.org/greenhouse-gas-emissions
- https://www.climate.gov/news-features/understanding-climate/climate-change-annual-greenhouse-gas-index#:~:text=Change%20over%20time,78%20percent%20of%20that%20increase.
- https://ourworldindata.org/co2-emissions
- https://ourworldindata.org/grapher/sea-level
- https://ourworldindata.org/grapher/imported-or-exported-co-emissions-per-capita?time=latest
- https://ourworldindata.org/grapher/change-co2-annual-pct
- https://ourworldindata.org/grapher/number-of-natural-disaster-events?country=Wildfire~Flood~Extreme+weather~Extreme+temperature~Dry+mass+movement~Drought~All+disasters+excluding+extreme+temperature~All+disasters+excluding+earthquakes~All+disasters
- https://ourworldindata.org/natural-disasters
- https://ourworldindata.org/temperature-anomaly
- https://www.bbc.co.uk/news/science-environment-45678338
- https://www.wri.org/insights/cop26-key-outcomes-un-climate-talks-glasgow
- https://www.wri.org/data/greenhouse-gas-emissions-over-165--years#:~:text=While%20the%20United%20States%20kept,annual%20emitter%20until%202005%2C%20when%E2%80%A6&text=Between%201850%20and%201960%2C%20the,particularly%20in%20the%20United%20States.
- https://www.bgs.ac.uk/discovering-geology/climate-change/how-does-the-greenhouse-effect-work/#:~:text=The%20contribution%20that%20a%20greenhouse,carbon%20dioxide%20(CO2
- https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Glossary:Kyoto_Protocol
- https://www.e-education.psu.edu/earth104/node/1262#:~:text=Overall%2C%20though%2C%20it%20is%20fairly,others%20just%20under%20a%20tenth.
- https://ocean.si.edu/through-time/ancient-seas/sea-level-rise#:~:text=Between%201900%20and%201990%20studies,at%203.4%20millimeters%20per%20year%20.
- https://www.who.int/news-room/fact-sheets/detail/ambient-(outdoor)-air-quality-and-health
- https://stats.stackexchange.com/questions/84076/negative-values-for-aic-in-general-mixed-model
