# Meta-Climate-Watch
A composite analysis of temperature anomaly vs. CO2 emissions and what actions can the global cement &amp; concrete industry do to reverse global warming trends.
by:  Romeo Siquijor (https://romeosiquijor.com)
 
## WHAT CAN THE CEMENT INDUSTRY (4TH LARGEST CO2 EMITTER) DO TO COMBAT GLOBAL WARMING?

A COMPOSITE ANALYSIS OF TEMPERATURE ANOMALY VS. CO2 EMISSIONS AND WHAT ACTIONS CAN THE GLOBAL CEMENT INDUSTRY DO TO REVERSE GLOBAL WARMING TRENDS. 

## OBJECTIVES:
- To present the trends of the negative impact of CO2 emissions and its potential impact to global warming that threatens the continuity of life on Earth.
- To explore the scientific approach using different forecasting models (ARIMA vs LSTM) to understand temperature dynamics through time series decomposition and identify key components contributing to global temperature anomaly.
- To evaluate the effectivity of the climate action strategies and efforts by the cement & concrete industry to avoid crossing the dangerous 2 degrees Celsius temperature anomaly threshold.

## PROBLEM STATEMENTS:
1.	Why is CO2 and other greenhouse gases (GHG) the biggest threat to the continuity of life on Earth?
2.	How can an industry (Cement & Concrete), traditionally emitting 5-8% of global CO2 helps in reversing global warming and achieve Net-Zero Emissions by 2050?

## DATASETS:
1.	Temperature Anomaly dataset source: “temperature_data.csv” from Berkeley Earth.
2.	Global CO2 Emissions dataset source:  “Global_Carbon_Budget_2023v1.0.xlsx” from Global Carbon Project.
3.	Pre-processed Data of Carbonation Sink:  "carbonation_data.csv" excerpt of dataset 2.

## METHODS:
### A.	Temperature Anomaly Forecasts
1.	ARIMA + FB Prophet – to forecast the temperature anomaly up to 2034.
2.	LSTM – to compare the forecast results of a neural network forecasting model vs ARIMA-Fb Prophet.

### B.	 Carbonation Sink Forecast
1.	ARIMA (Auto Regressive Integrated Moving Average) + STL (Seasonal Trend) – are used to forecast how much CO2 can the revolutionary decarbonizing concrete formulation help in lowering emission rates through with carbonation sink process up to 2034, in line with NZE (Net-Zero Emission) goal of the GCCA (Global Cement & Concrete Association) by 2050.  
2.	LSTM – to compare the forecast results of a neural network forecasting model vs ARIMA-STL.

## The Dangerous 2 degrees Celsius Tipping Point 
 
The continuity of life on Earth is under threat attributed to the looming 2-degree Celsius temperature anomaly rise, primarily driven by the escalating emissions of carbon dioxide (CO2) and greenhouse gases (GHGs). Over the past three decades, Earth's temperature has experienced a rapid ascent known as the hockey-stick phenomenon.  It is largely attributed to human activities such as burning fossil fuels, deforestation, and industrial processes. This anthropogenic interference intensifies the greenhouse effect, trapping heat in the atmosphere and leading to a warming planet.
 
NASA underscores the catastrophic implications of a 2-degree Celsius temperature anomaly. The rise poses severe risks, including more frequent and intense heatwaves, droughts, rising sea levels, disruptions to ecosystems, salinization, and an increased frequency of extreme weather events. These changes could have devastating effects on biodiversity, food security, economy, safety, and threaten the livelihoods of communities across the globe.[1]
 
## Takeaways:
•	Temperature anomaly is the combined land and sea temp variance compared to the last 30 years by grid.
•	Earth crossed the 1-degree temp. anomaly in 2013.
•	In 2023, temp. anomaly is at record high of 1.36 degrees Celsius.
•	NASA says that, 2 degrees Celsius temperature anomaly is catastrophic to life on Earth.
 
## 2035-2070 Apocalyptic Scenario of CMIP6 Model
Scientists, alarmed by the trajectory of current emissions, forecast that we could breach the critical 2-degree threshold between 2035 and 2070 if significant interventions are not implemented urgently.  

The Berkeley Earth Project is the main source of the temperature anomaly datasets used in this study.[2]
 
## Earth’s Temperature Anomaly Continues to Rise
Global temperature anomaly has increased by about 2 degrees Celsius since 1850 and highest in the last 3 decades.  Using ARIMA with FB Prophet model shown below, we can validate the continued uptrend of temperature anomaly.
 
## ARIMA (2,1,1) with Drift, Lag analysis, and residuals
The residuals in the model are generally small and random, with no obvious patterns.  There is a slight upward trend in the residuals over time. Overall, the graph suggests that the model could be a good fit for this temperature anomaly dataset analysis. However, there are a few outliers which suggest that the model could be improved.
 
## Correlogram:  ACF, Standard Residuals, ACF of R, and p values for Ljung
 
ACF Plot:  autocorrelation of the temperature anomaly is high at short time lags and then decreases over time. This means that the temperature is very similar at short time lags, but then becomes progressing dissimilar at longer time lags.
 
Standard residuals: there are a few outliers in the model. Typically, any standardized residual with value greater than 3 can be an outlier.
ACF of Residuals: no significant autocorrelations in the residuals at any lag.
p values for Ljung-Box statistics: all the p-values are greater than 0.05, therefore the model is statistically significant.
 
## Temperature Anomaly Comparing ARIMA vs LSTM 
 
As compared to LSTM model, ARIMA-FB Prophet shows a better statistical forecast for this temperature anomaly time series.
The preference for ARIMA (AutoRegressive Integrated Moving Average) over LSTM (Long Short-Term Memory) in forecasting longer time series, like temperature anomalies, can be attributed to several factors:

Firstly, ARIMA excels in capturing linear trends and patterns within the data. For longer time series, where underlying trends might be more linear or exhibit smoother variations, ARIMA's capability to model such relationships becomes advantageous. Temperature anomalies, often influenced by gradual changes in climate patterns, may manifest as linear trends over extended periods. ARIMA's ability to effectively represent these trends contributes to its success in longer-term forecasting.
Moreover, the assumption of stationarity, inherent in ARIMA, aligns well with certain characteristics of temperature anomaly data. While climate conditions can evolve over time, certain aspects of temperature anomalies might exhibit relative stability, making the stationarity assumption reasonable for specific time spans. ARIMA's proficiency in handling stationary time series becomes valuable in scenarios where the statistical properties of the data remain relatively constant over extended periods.
Another contributing factor is the simplicity of relationships within the temperature anomaly data. ARIMA is a parsimonious model, meaning it tends to prefer simpler explanations for observed patterns. In cases where the temperature anomaly is governed by more straightforward dynamics or where the relationship with historical data can be adequately captured using linear models, ARIMA's simplicity becomes an asset.

Additionally, the sheer volume of data available in longer time series can play a role in ARIMA's success. With an extended historical record, ARIMA has more information to discern patterns and establish relationships between past and future observations. This abundance of data empowers ARIMA to make more informed predictions over longer horizons.

While LSTM and other neural network-based models excel at capturing complex, non-linear patterns and dependencies, they may be more computationally intensive and prone to overfitting, especially when dealing with smaller datasets. In contrast, ARIMA, with its simplicity and emphasis on linear relationships, can provide reliable forecasts for longer time series, such as temperature anomalies, under conditions where the underlying dynamics align with its modeling assumptions. The effectiveness of ARIMA in this context underscores the importance of selecting a forecasting model that aligns with the specific characteristics of the data at hand.

### A.	ARIMA + FB Prophet Model Validate Temperature Anomaly Uptrend
 
The collaboration between the ARIMA (AutoRegressive Integrated Moving Average) and Facebook Prophet models creates a powerful synergy in the validation of temperature anomaly uptrends, offering a nuanced and comprehensive understanding of the underlying patterns in the data.
ARIMA, with its strength in capturing linear trends and statistical significance, contributes a foundational framework to the modeling approach. If temperature anomalies exhibit a gradual and consistent increase over time, ARIMA's ability to discern linear relationships becomes invaluable. It brings a quantitative measure of statistical significance to the analysis, reinforcing the reliability of trends identified within the dataset.

On the other hand, Facebook Prophet brings flexibility and adaptability to the modeling process. Its design allows for the accommodation of various patterns and seasonality inherent in temperature anomaly data. The model's ability to account for external factors, such as holidays and special events, aligns with the complexities often found in climate-related datasets. Prophet's unique component decomposition capability breaks down the time series into its fundamental components—trend, seasonality, and holidays—offering a more granular and interpretable view of the underlying patterns.
The combination of ARIMA and Prophet introduces an ensemble effect, leveraging the complementary strengths of each model. While ARIMA excels in capturing linear trends and providing statistical validation, Prophet accommodates more intricate patterns and external influences. This ensemble approach enhances the overall robustness and accuracy of the forecast.

The validation process gains further credibility through consistency. If both ARIMA and Prophet independently confirm an uptrend in temperature anomalies, it serves as a powerful validation mechanism. The convergence of signals from two distinct models not only reinforces the existence of an uptrend but also instills confidence in the forecast.

Moreover, the combined model allows for a dynamic and adaptive modeling strategy. ARIMA's strengths in handling linear trends complement Prophet's ability to adapt to changing patterns over time. In cases where gaps or irregularities exist in the temperature anomaly dataset, Prophet's robustness in handling missing data ensures a more reliable and continuous analysis.

In essence, the ARIMA + Facebook Prophet model combination represents a harmonious blend of linear trend detection, statistical rigor, flexibility, and adaptability. This collaborative approach elevates the validation of temperature anomaly uptrends, providing a holistic and reliable foundation for understanding the evolving dynamics of climate-related data.
 
### B.	LSTM Model Shows Faster Uptrend Compared to Observed Data
 
The LSTM (Long Short-Term Memory) model is good for its ability to capture intricate patterns and complex interdependencies in time series data.  But applying LSTM in our model exhibits a faster uptrend in temperature anomaly compared to real observed data. I believe that this phenomenon arises from the model's inherent characteristics and the complexities involved in training and interpreting deep learning models.  I suspect that LSTM responded sensitively to short-term fluctuations, leading to a quicker upward trend in its forecasts compared to real-observed data.

LSTM can be highly responsive to fluctuations, adjusting their internal states based on recent observations. In the context of temperature anomaly, where short-term variations can be influenced by various factors like weather patterns or seasonal changes, the model might amplify these fluctuations, resulting in a faster perceived uptrend.

Based on my research, the complexity of the LSTM architecture considers multiple layers and memory cells – which could capture and remember subtle patterns that might be overlooked by simpler models. While this is a strength in capturing intricate relationships, it can also lead to the model learning from noise or short-term irregularities, potentially causing it to project a more rapid uptrend compared to the actual observed data, as what we achieved in the model.

It is important to note that the performance of deep learning models, including LSTMs, heavily depends on the quality and quantity of the training data. If the training data contains biases, outliers, or noise, the model might inadvertently learn from these features, impacting its ability to generalize accurately to unseen data.
Interpreting and fine-tuning deep learning models like LSTMs can be challenging due to their black-box nature. The intricate network of weights and connections within the model makes it less transparent compared to traditional statistical models like ARIMA. As a result, unexpected behaviors, such as a faster uptrend in our model, might occur, and understanding the precise reasons behind these behaviors can be complex.
 
## The Invisible Enemies
 
The drastic increase in CO2 and GHG concentrations in the atmosphere enhances the natural greenhouse effect, trapping more heat and causing the planet's temperature to spiral upwards.

The mechanism of temperature rise is intricately linked to the greenhouse effect, wherein certain gases, including CO2, trap outgoing infrared radiation from the Earth's surface, preventing it from escaping into space. As these concentrations rise due to human activities, more heat is retained, causing a gradual but impactful increase in global temperatures.

In the year 2023, the Mauna Loa Observatory, a critical station for monitoring atmospheric CO2 levels, reported a concentration exceeding 420 parts per million (ppm). This means that for every 1 million gas molecules in the atmosphere, approximately 420 of them are now CO2. This milestone reflects the alarming trend of rising CO2 emissions and their accumulation in the atmosphere, further intensifying the greenhouse effect. [3]

The concept of parts per million (ppm) signifies the proportion of a specific gas in the overall composition of the atmosphere. In the case of CO2, a concentration of 420 ppm indicates a significant increase from pre-industrial levels, contributing to the enhanced trapping of heat. This rise in greenhouse gas concentrations correlates with a concerning trajectory in global temperatures.

To maintain a safe and stable climate, scientists emphasize the importance of keeping CO2 levels below a critical threshold. The widely acknowledged target is to stay below 450 ppm. If we surpass this threshold, there is an increased risk of triggering a dangerous 2-degree Celsius temperature rise, which could lead to severe consequences such as more frequent and intense heatwaves, rising sea levels, melting polar ice caps, salinization, and disruptions to ecosystems that threatens the global economy and life in general.
 
## The Cement Industry, the 4th Largest CO2 Emitter
 
The cement and concrete industry, traditionally responsible for approximately 5-8% of global CO2 emissions, is at a pivotal industry where innovation on sustainability practices can play a transformative role in reversing global warming and achieve Net-Zero Emissions by 2050.

The cement production process, a key contributor to CO2 emissions, involves the heating of limestone and other raw materials in kilns at a temperature between 1338 °C and 1450 °C, releasing substantial amounts of carbon dioxide. However, the industry is actively exploring and implementing strategies to mitigate its carbon footprint.
In 2023, global CO2 emission is calculated at 37.5 GtCO2, of which 2.5 GtCO2 (6.6%) is attributed to cement production.  The cement & concrete industry is expected to have 1.6% emission decrease in 2023 due to decarbonization efforts and the decline in Chinese cement production as an aftermath of COVID-19.  China’s cement output dropped 10.5% to about 2.13 billion tpy (tons per year) in 2022 and continues with the same trend in 2023. The ongoing rate of decline might be even higher.  The decline in Chinese cement production is still attributed to the impact of COVID-19, slowing down construction projects overall in China. [4]
 
##What is the Global Cement & Concrete Industry Doing to Reverse Global Warming?

While there has been a notable decrease in CO2 emissions of the cement and concrete industry in 2023, it remains a significant fraction of the total global CO2 output. The commitment to reduce emissions is growing, and the industry is actively engaged in partnerships, research, and investments to accelerate the transition towards a low-carbon future.  But achieving Net-Zero Emissions by 2050 requires a collaborative effort involving governments, industries, and communities. The cement and concrete sector's commitment to innovation, sustainable practices, and the adoption of greener technologies is a positive step toward mitigating climate change and realizing a more environmentally responsible future. As these efforts continue, the industry aims to play a crucial role in not only meeting but potentially exceeding global emissions reduction targets. [5]

In response to the NZE (Net-Zero Emissions) by 2050 mission and to combat climate change, the cement and concrete industry is undergoing a transformative journey, implementing a range of initiatives to significantly reduce CO2 emissions such as:

•	Promoting the Use of Alternative Fuels: recognizing the environmental impact of traditional fossil fuels used in the calcination and heating processes, the industry is actively promoting the adoption of alternative fuels. By incorporating materials like biomass, waste-derived fuels, and even non-recyclable plastics, cement plants are reducing their reliance on traditional energy sources, thereby mitigating CO2 emissions associated with the production process.

•	AI and ML for Clinker Production Optimization: by harnessing the power of Artificial Intelligence (AI) and Machine Learning (ML), the industry is optimizing clinker production processes to achieve greater efficiency and reduced energy consumption. By leveraging advanced analytics, real-time monitoring, and predictive modeling, cement plants can fine-tune their operations, minimizing energy requirements and subsequently lowering CO2 and greenhouse gas emissions.

•	Reforestation and Environmental Restoration: beyond operational changes, the industry is actively engaging in reforestation, afforestation, and the restoration of local environments. Recognizing the role of forests in absorbing CO2, cement and concrete producers are contributing to projects aimed at preserving and restoring natural ecosystems. This holistic approach not only offsets emissions but also fosters biodiversity and environmental resilience.

•	Development of CCUS Systems: Carbon Capture, Utilization, and Storage (CCUS) technology is emerging as a critical component in the industry's decarbonization strategy. Cement plants are exploring the implementation of CCUS systems to capture CO2 emissions at the source and either store them underground or repurpose the captured carbon for beneficial uses, further minimizing the industry's carbon footprint.

•	Producing Decarbonizing Concrete: The forefront of innovation lies in the development of decarbonizing concrete. Researchers and industry leaders are investing in novel formulations that either use alternative, low-carbon binders or actively absorb CO2 during the curing process. By incorporating innovative materials and processes, this next generation of concrete aims to significantly reduce the overall carbon impact associated with construction projects.  
The core focus of this project is to analyze how much CO2 can be reduced through carbonation process by simply adding fly ash, slag, biochar, and other geopolymers in the concrete mix, technically making concrete a better carbon absorber.

 
## Decarbonizing Concrete:  Permanently Burying CO2

One of the key innovations in the cement and concrete industry is the introduction of alternative, low-carbon or carbon-neutral cement and concrete products. These innovative materials, such as geopolymer cements or those incorporating supplementary cementitious materials like fly ash, slag, and biochar, aim to reduce the reliance on traditional Portland cement, which is a major source of CO2 emissions by this industry. By adopting these alternatives, the cement & concrete industry can significantly decrease its carbon emission.  

The main goal of this study is to analyze if the climate action strategies and effort of the cement and concrete industry is effective, particularly in measuring impact of carbonation sink.  Carbonation process takes place when carbon dioxide is absorbed by concrete. It is the chemical reaction that happens when carbon dioxide is absorbed by calcium hydroxide and hydrated calcium silicate in concrete. By calculating the potential contribution of carbonation sink, we can conclude if the cement and concrete industry will meet their pledge of reducing 25% of the industry’s CO2 emission by 2030 and Net-Zero by 2050.   

For the first model, I used ARIMA (AutoRegressive Integrated Moving Average) and STL (Seasonal and Trend decomposition using Loess).  Both ARIMA and STL are powerful tools for analyzing and forecasting time series data, and combining them can provide a more robust approach, particularly when dealing with complex and seasonally influenced time series.

1.	ARIMA (AutoRegressive Integrated Moving Average):
ARIMA is a statistical model used for time series forecasting. It involves three main components: AutoRegressive (AR) terms, Integrated (I) terms, and Moving Average (MA) terms. These components capture the autocorrelation, trend, and seasonality in the time series data, respectively.

2.	STL (Seasonal and Trend decomposition using Loess):
STL is a decomposition method that separates a time series into three main components: Seasonal, Trend, and Residual. The Seasonal component represents the recurring patterns at fixed intervals, the Trend component captures the overall direction or tendency of the data, and the Residual is the leftover or noise after removing the seasonal and trend components.

## Combined ARIMA-STL:

ARIMA-STL combines the ARIMA model with the STL decomposition. The seasonal and trend components obtained from STL are used to inform the ARIMA model. This approach is particularly beneficial when dealing with time series that exhibit complex seasonal patterns and trends. By decomposing the time series with STL first, the ARIMA model can focus on capturing the remaining variability, potentially improving the accuracy of the forecast.  However, the forecast doesn’t seem to fit the model.
Based on ARIMA-STL Model, Concrete Carbonation sink forecast would be at least ~200 MtCO2 (by 2030) ~300 MtCO2 (by 2050). 
 

### Takeaways:

•	ARIMA-STL forecast started lower than observed dataset primarily driven by the disparity of data.
•	The model shows that by 2030, concrete carbonation sink could sequester or absorb at least >200 MtCO2 (lower than most recent data in 2021 of 239).
•	By 2050, the ARIMA-STL forecast estimates ~0.2 to 0.5 (median: .3) GtCO2 absorption. 
 
Based on LSTM Model, Concrete Carbonation sink forecast by 2030 would be at least ~300 MtCO2 and ~550 MtCO2 by 2050.
 
### Takeaways:

•	Huang’s model has more updated datasets (up to 2021, showing Carbonation sink at 239 MtCO2).
•	Using LSTM model, by 2030 concrete carbonation sink could sequester or absorb at least 300 MtCO2 (100 MtCO2 higher than the ARIMA-STL Model).
•	By 2050, the LSTM forecast estimates ~400 to 700 (median: 550) MtCO2 absorption.
 
## Conclusion:

The net carbon offsets by the cement industry are 55.1 % of its total emissions.  The carbonation sink represents 25% of it.  Carbonation sink is expected to increase as the use of alternative cementitious materials & concrete mix with better CO2 absorption increases, therefore the LSTM model shows a more promising forecast.

By simply adding fly ash, slag, biochar, and other geopolymers in the concrete mix, according to other scientific studies, concrete carbonation can help reduce between 0.1 to 1.4 gigatons of CO2 by 2050.  

## Our forecast shows: 

- ARIMA-STL model:  ~0.2 to 0.5 (median 0.3) GtCO2 by 2050.
- LSTM model:  ~0.5 to 0.7 (median 0.55) GtCO2 by 2050.

With the other decarbonization efforts such as using alternative fuel, AI & ML to optimize cement production, alternative cementitious materials that require less heat, reforestation/afforestation/ environmental restoration, and CCUS (Carbon Capture & Storage) solutions -- the Cement & Concrete industry is well on its way towards its NZE (Net Zero Emissions) mission by 2050.


## Caveat and Call to Action:

While the effort of the cement and concrete industry can help delay crossing the dangerous tipping-point of 2 degrees Celsius, other industries like coal, oil, and gas sectors need to follow suit. Otherwise, as what Barrack Obama said: 

# “We are the first generation to feel the effect of climate change and the last generation who can do something about it.”
 
### References:

[1] Tabor, A. (2023, September 30). NASA study reveals compounding climate risks at two degrees of warming - NASA. NASA. https://www.nasa.gov/centers-and-facilities/ames/nasa-study-reveals-compounding-climate-risks-at-two-degrees-of-warming/#:~:text=If%20global%20temperatures%20keep%20rising%20and%20reach%202,to%20understand%20how%20different%20climate%20effects%20might%20combine.

[2] Hausfather, Z. (2023, August 14). Are temperatures this summer hotter than scientists expected? - Berkeley Earth. Berkeley Earth. https://berkeleyearth.org/are-temperatures-this-summer-hotter-than-scientists-expected/

[3] Mauna Loa carbon dioxide forecast for 2023. (2021, January 8). Met Office. https://www.metoffice.gov.uk/research/climate/seasonal-to-decadal/long-range/forecasts/co2-forecast

[4] Staff, C. B. (2022, November 11). Analysis: Global CO2 emissions from fossil fuels hit record high in 2022. Carbon Brief. https://www.carbonbrief.org/analysis-global-co2-emissions-from-fossil-fuels-hit-record-high-in-2022/

[5] Psci. (2020, November 3). Cement and Concrete: the Environmental Impact — PSCI. PSCI. https://psci.princeton.edu/tips/2020/11/3/cement-and-concrete-the-environmental-impact

