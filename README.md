# WSB1535: Trapping efficacy of invasive crows is affected by environmental factors and deployment history
Article: https://wildlife.onlinelibrary.wiley.com/doi/10.1002/wsb.1535

House crows (Corvus splendens) are considered an invasive species and are prevalent in many countries. Existing crow management measures range from food limitation, habitat modification and direct population control. The latter method provides a more immediate solution particularly in nesting locations where crow attacks occur more frequently. Crow ladder traps are widely adopted to capture crows, but a thorough examination of the environmental conditions that optimise trapping efficacy is lacking. We assessed factors affecting crow trap efficacy in Singapore to better advise future deployment strategies of crow traps. We obtained data from 170 crow trapping operations including the identities of the contractors conducting the trapping operations, operation start date, crow density, intensity of bird feeding, various land use cover proportions and an index to quantify the spatial-temporal proximity to previous trapping operations. We used a spatial gamma generalised linear mixed model (GLMM) to determine the factors affecting the daily number of crows captured and a spatial binomial GLMM to determine the factors affecting the probability that crows will be captured. 

## Description
This data set contains a pair of location coordinates, 15 predictor variables and one response variable of 170 crow ladder traps. The 15 variables were used in building two models – (1) a zero-truncated general linear model (GLM) with a Gamma error distribution and log link function for all non-zero values of crow trapping efficacy, and (2) a GLM with binomial error distribution for zero and non-zero trapping efficacy values. The number of crows caught per day is the response variable that is a measure of trap efficacy.

Both sets of models were run together with all combinations of variables examined and models were evaluated using the Akaike Information Criterion. To account for spatial autocorrelation, we refitted our most parsimonious models using a spatial generalised linear mixed model (GLMM), which utilises the location coordinates provided in the dataset.

This comma-separated-value (csv) file can be loaded into R as a data frame, where the first descriptive row is skipped and the second row provides the variable names. The data frame can be used directly for building a generalised linear model to model crow trap efficacy and conducting model selection. Spatial generalised linear mixed models can also be constructed from this data frame by including the location coordinates. The variables are as follows:

Index number is a unique identifier for each trap, numbered from 1 to 170.

X and Y coordinates were reprojected to a SVY21 coordinate system, where overlapping traps’ coordinates were displaced by 1m northwards and eastwards to avoid zeros in subsequent logarithmic calculations.
Multiple contractors were hired by NParks to deploy and operate the crow ladder traps. Each contractor builds their own ladder traps with slightly different dimensions and trapping methods that were otherwise largely similar. Contractors B and C were grouped together since their standalone sample sizes were small (Table 1). To standardise comparisons, crow trap efficacy with no live crow bait was not considered in the study, though they were included in calculating the proximity index.

The operation start date, referring the date of trap deployment, were presented in Julian date format (yyddd). Sine and cosine transformations were applied to the trap deployment dates to account for seasonal variations.
Crow population density (crows per hectare) was estimated from data by Tan et al. 2020. We obtained the average house crow density for each trapping location by averaging across the overlapping 1km2 cell and the eight adjacent cells (i.e., an average of nine cells).

Landscape variables were calculated at two scales (250m and 500m). The number of feeding incidents were collated from a NParks public feedback database between March 2022 to June 2023. The percentage cover of land uses at a 250m and 500m radius were calculated with pixel values extracted from a high-resolution map of Singapore’s terrestrial ecosystems (Gaw et al. 2019). Built up area included roads, buildings and other urban structures, where human-manged vegetation included vegetated areas that are routinely managed (e.g., planted and maintained by pruning) and utilized by humans, such as urban parks and gardens. Tree canopy cover was also considered.

Spatial-temporal index of proximity (STIP) was also calculated as a function of the time interval between each trap and its previous trap as well as the distance between adjacent traps, across all prior traps. A greater value of STIP corresponds to a smaller interval between the trap and the previous one, a smaller distance between adjacent traps, and greater number of prior traps.
Crow trap efficacy was defined as the total number of crows caught per active day of operation. Inactive days were when the trap was not monitored or operated (e.g. weekends) or days of inclement weather were excluded. All traps were deployed between March 2022 to June 2023.

The presence of other birds (Javan myna, rock pigeon) in the trap were also noted. 

## Data Sources
Land use variables:

Gaw LY-F, Yee ATK, Richards DR (2019). A High-Resolution Map of Singapore’s Terrestrial Ecosystems. Data 4, 116. doi:10.3390/data4030116

Feeding count:

National Parks Board (2023). NParks Customer Management System - Wildlife Management: Urban Birds [Dataset].

Population density:

Tan HZ, Low G, Sadanandan K, Rheindt F (2020). Population assessment of the house crow, Corvus splendens, in Singapore. Malayan Nature Journal 72, 133–142.
