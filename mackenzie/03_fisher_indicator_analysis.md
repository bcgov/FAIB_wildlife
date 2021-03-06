---
title: "Mackenzie TSA Fisher Indicator"
author: "Tyler Muhly"
date: "20/01/2022"
output:
  html_document:
    keep_md: yes
  word_document: default
---



## Mackenzie Timber Supply Review Fisher Indicator Analysis
Here I estimate and report on indicators of fisher (*Pekania pennanti*) territory occupancy to support the Mackenzie timber supply review. Fisher are a species of concern to First Nations in the region, and to the governments of British Columbia and Canada. First Nations requested an analysis to assess the potential influence of future simulated forest harvest on fisher as part of the timber supply review. This analysis is for both the Columbian population of fisher that is currently red-listed (i.e., extirpated, endangered, or threatened) by the [BC Conservation Data Centre](https://a100.gov.bc.ca/pub/eswp/reports.do?elcode=AMAJF01025), and the boreal population that is currently blue-listed (i.e., special concern) by the [BC Conservation Data Centre](https://a100.gov.bc.ca/pub/eswp/reports.do?elcode=AMAJF01025).

Fisher territory occupancy was estimated using the model developed by [Weir and Courbold 2010](https://wildlife.onlinelibrary.wiley.com/doi/abs/10.2193/2008-579), where the percentage of a fisher territory that is wetlands or less than 12 year old logged forest (i.e, "open area") was found to be a useful indicator of whether a territory was occupied by fisher. Territories with more wetland or logged forest were less likely to be occupied. The data used to develop this model was collected northwest of the town of Mackenzie, in the late 1990's and early 2000's. 

An important limitation on the use of this model as an indicator of fisher occurrence is that it does not consider the quality of habitat within territories. For example, this approach does not evaluate the presence of large trees with cavities that are necessary for fisher denning. Therefore, even though the probability of occupancy for a given territory may be high, it does not mean that all of the habitat features necessary for fisher survival and reproduction are provided. This is important for interpretation of results, because, for example, an entire fisher territory could be completely logged and have a zero probability of occupancy for 12 years, but then could score a 100% probability of occupancy at year 13. However, realistically for the territory to be occupied it would require some stands at least 100 years old to provide denning cavities. Nevertheless, the model broadly serves as a useful indicator to evaluate fisher occurrence across a landscape based upon forest harvest history. 

I assessed two forest harvest simulations, the 'base case' and 'south partition-yield 75% scenario', where each simulation represented different inputs to a spatial timber supply model. The base case approximated current forestry practices in the Mackenzie timber supply area (TSA) carried forward into the future. In particular, existing legal requirements on forest harvest were used to define where forestry activities could, or could not occur in the future. The south partition-yield 75% scenario reduced stand yield by 25% and included a south partition in the Mackenzie TSA. 



## Methods
Fisher territories range in size and shape based upon local habitat conditions, but here I created a standard territory size across fisher range within the TSA. Each territory is hexagon in shape and 30km^2^ in size (i.e., an average fisher home range size; www.bcfisherhabitat.ca). Although not a biologically relevant shape, these may be considered as fisher-equivalent territory areas (FETAs), which represent the amount of area and habitat that could theoretically support a female fisher. 



The current and simulated future area of wetlands and logged forest less than 12 years old was calculated within each FETA. Data on current logged forest within the [Mackenzie TSA](https://catalogue.data.gov.bc.ca/dataset/fadm-timber-supply-area-tsa) was obtained from the [harvested areas](https://catalogue.data.gov.bc.ca/dataset/harvested-areas-of-bc-consolidated-cutblocks-) dataset. Data on wetlands was obtained from the [forest inventory data](https://catalogue.data.gov.bc.ca/dataset/vri-2020-forest-vegetation-composite-layer-1-l1-), where the B.C. land cover classification scheme was used to identify current non-treed wetland areas, which are assumed to be stable throughout the simulation period. 

Data on future cutblocks in the base case and south partition-yield 75% scenarios was obtained from the Mackenzie timber supply review spatial timber supply model at decadal intervals. For each scenario and future decade, I calculated the amount of area logged that is less than 12 years old by adding the total amount of area logged in the previous decade (i.e., the area logged in the last 10 years) to 20% of the area logged two decades prior (i.e., the area logged that is 11 and 12 years old). This assumes the amount of area logged over a decade is similar each year.   









FETA occupancy was calculated using the model developed by Weir and Courbold 2010, where the relative probability of occupancy is a function of the percentage of open area within a FETA. The percentage of open area was calculated as the amount of area logged in the previous 12 years added to the area of non-treed wetland and divided by the area of a FETA.



The sum of probability of occupancy values of all FETAs in the Mackenzie TSA was calculated for each decade. This was used as an indicator of the total number of potentially occupied FETAs.  



## Results
Currently, the relative probability of fisher occupancy of FETAs was relatively low in the southwest portion of the Mackenzie TSA, and relatively high in the east-central and northern portions of the TSA. 

![](03_fisher_indicator_analysis_files/figure-html/base case plot occ 2020-1.png)<!-- -->

### Trends in Total Probability of Occupancy
In the base case scenario, the sum of the probability of occupancy values of all FETAs (i.e., the total probability of occupancy) decreased across the simulation period. From 2020 to 2090, the total probability of occupancy of FETAs in the base case decreased from approximately 820 to approximately 780. In the south partition-yield 75% scenario, the total probability of occupancy was essentially flat between 2020 to 2090, but with fluctuations across decades.

![](03_fisher_indicator_analysis_files/figure-html/plot occ over time-1.png)<!-- -->

### Base Case Scenario Probability of Occupancy Maps 
In the base case simulation, the relative probability of occupancy increased in FETAs in the western portion of the TSA in 2040. However, relative probability of occupancy decreased in some FETAs in the east-central portion of the TSA.

![](03_fisher_indicator_analysis_files/figure-html/base case plot occ 2040-1.png)<!-- -->

In 2060, the relative probability of occupancy increased in FETAs in the southern portion of the TSA, but the relative probability of occupancy decreased in central portions of the TSA. 

![](03_fisher_indicator_analysis_files/figure-html/base case plot occ 2060-1.png)<!-- -->

Relative probability of occupancy remained relatively low in central portions of the TSA in 2080, and again declined to lower values in the southern portions of the TSA. Throughout the duration of the base case simulation, relative probability of occupancy of FETAs remained relatively high in northern portions of the TSA. 

![](03_fisher_indicator_analysis_files/figure-html/base case plot occ 2080-1.png)<!-- -->

### South Partition-Yield 75% Scenario Probability of Occupancy Maps
In the south partition-yield 75% scenario, the relative probability of occupancy decreased in FETAs in the central portion of the TSA and increased in FETAs in southern portions of the TSA in 2040. 

![](03_fisher_indicator_analysis_files/figure-html/iaf plot occ 2040-1.png)<!-- -->

In 2060, the relative probability of occupancy increased in FETAs in the central portion of the TSA. 

![](03_fisher_indicator_analysis_files/figure-html/iaf plot occ 2060-1.png)<!-- -->

Relative probability of occupancy decreased in south-central portions of the TSA in 2080. Throughout the duration of the south partition-yield 75% scenario simulation, relative probability of occupancy of FETAs remained high in central and northern portions of the TSA. 

![](03_fisher_indicator_analysis_files/figure-html/iaf plot occ 2080-1.png)<!-- -->

## Discussion
In general, the simulated future probability of occupancy of FETAs decreased in central portions of the TSA and increased in southern portions of the TSA in both scenarios. This reflected a shift in forest harvest by the model from southern to central portions of the TSA in the near and mid-term. Overall, the south partition-yield 75% scenario resulted in an approximately 5% greater total probability of occupancy of FETAs than the base case in the mid- to long-term.

An important limitation of the occupancy model approach used here is that it does not consider habitat quality within a FETA. A high probability of occupancy does not necessarily mean there is sufficient habitat within a FETA to support fishers biological needs. These results should therefore be used with significant caution.
