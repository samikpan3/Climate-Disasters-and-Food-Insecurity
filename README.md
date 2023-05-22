# Disaster and Food Insecurity 
###  Research Question: 
What are the impacts of disaster(natural) on the food security as defined by the Food and Agriculture institution(FAO)
The independent variable is the magnitude of the disasters that occurred at a given year and given country. The dependent variable would be the prevalence of food insecurity measured by indicators : prevalence of undernourishment and prevalence of severe food insecurity, and prevalence of moderate food insecurity. These values are measured by FAO. 

## Dataset Sources: 
1. “EM-DAT, CRED.” EM-DAT Public, UCLouvain, Brussels, Belgium, 2022, https://public.emdat.be/data.
EMDAT Centre for Centre for Research on Epidemiology of Disasters is a non profit that later became one of the World Health Organization Collaborating Centre . EMDAT keeps the database for all occurances for natural disasters and quantifies its effects. As of 2022, it has recorded over 22,000 mass disasters in the world from 1900 to the present day. 

2. UN FAO. “FAOSTAT.” Food and Agriculture Organization of the United Nations, 2022, https://www.fao.org/faostat/en/#data/FS.  
The Food and Agriculture Organization (FAO) is a specialized agency of the United Nations leading international efforts to defeat hunger. FAO's goal is to achieve food and security for all and make sure that people have regular access to enough high-quality food and lead active, healthy lives. It keeps meta deta on global hunger, 

## ABOUT THE RESEARCH
  Hunger is a global issue and millions of people are suffering from it. Food insecurity is defined by FAO as the lack of availability at all times of adequate world food supplies of basic foodstuffs to sustain a steady expansion of food consumption and to offset fluctuations in production and prices. Similarly, climate change is a pressing issue and its frequency is increasing. These disasters can have devastating impacts on food insecurity. This research paper, aims to address this issue and examine the impact of disasters on food insecurity (specifically % of malnourishment). This can help us anticipate the impact of disasters on food insecurity which can help us prepare and direct resources appropriately in disasters impacted areas. 
  
  ## VARIABLE OF INTEREST
  * Percentage of malnourishment (undernourish%)
  * Disaster Type and Magintude(Mag)
  * Pecentage of moderately and severely undernourished population (m/s_ finsec%)
  * Consumer Price Index (CPI)
  * Per Capita Food Production (pcal_fprod)
  
##Solution Technologies
Github, Google Colab,Tableau, Python, Zoom, Canvas, Google docs.

## Analytic Approach and Conclusion 
In the project, we first transformed the FOASTAT_data.csv from long format to wide format and then merged it to the dataset emdat.csv to get one dataset.
And in this dataset, there are many NULL values especially in the diasaster magnitude column(Mag). As each type of disaster has different scale to calculate the magnitude, we imputed the values using MICE imputation by for each type of disaster(DisType) and also normalized the data using MinMaxScaler(). This gives us the final data which can be trained further. 
Coming to the modeling, we splitted the data into train and test sets using traintestsplit() of sklearn and then trained using multiple models like CNN, random forest, linear regression and multiple linear regression. As the data has more non-linearity, CNN and random forest best fitted the data with a mean squared error of 0.05.
In addition to this 3 types of disasters namely flood, storm and earthquake and trained the models using these grouped data. From this analysis, the mean squared error of flood and storm is much closer to 0. Hence, we can conclude that flood and storm has much impact on food insecurity compared to earthquake

## Contents of the Repository
* FOASTAT_data.csv - food insecurity dataset
* emdat.csv - disasters dataset
* final_normalized_data - final data with a column named normalized having the normalized values of magnitude.
* final_project.ipynb - the colab notebook we worked on.
* visualizations - tableau file containing some visualizations.
* references - file having all the references and data sources.
* Data 5100 Analysis Project Presentation

