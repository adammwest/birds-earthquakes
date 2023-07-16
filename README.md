Predicting Earthquakes with Birds 

Project Question 
Can Bird movement predict any earthquakes features?

Earthquake data
https://www.emsc-csem.org/

Weather Data
https://www.eswd.eu/

Bird Data 
they have a rich white stalk database
https://www.movebank.org/cms/movebank-content/env-data

Linking the events with animals
to complete this analysis the data needs to be merged tempro-spartially.
earthquake data first 35KM +/-180 mins each side of the earthquake event,
then any weather data 

according to 
https://onlinelibrary.wiley.com/doi/full/10.1111/eth.13078#:~:text=Potential%20short-term%20earthquake%20forecasting%20by%20farm%20animal%20monitoring,in%20animal%20behavior%20...%204%204%20DISCUSSION%20
"A collective of domestic animals repeatedly showed unusually high activity levels before earthquakes, with anticipation times (1–20 hr) negatively related to distance from epicenters (5–28 km)."
35km was increased from 28km which was proposed by the paper 

Resampling
I resampled the data at exactly their closest [1,5,10,15,30,45,60] minute interval this meant the data was much easier to work with as each time difference was constant

Input Features
height/ coodinates/ speed values 
speed category using BIRCH clustering algorithom 

Prediciton Features
distance from earthquake
magnitude
time to event

Modelling 
earthquake prediction trained using nueral networks 


Training method 
find animal create cluster based on animal movement patterns exclude eq events 
how close is event to normal animal movement patterns 

split data into each earthquake event and by each hour 


TODO
* KFOLD validation per event,hour 
* include +/-20H for training induvidual animal model
* visualisation of bird movement as an animation with the eq event 
* train model and graph results
* stats of how many early warning eqs the birds successfull managed to predict
* make dockerised click app that takes long,lat,height data and predicts eqs features
* make final report 






















