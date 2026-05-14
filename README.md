# Känzig Replication and Extension README
----------------------------------------
Joseph Nolan and Grayson Maryanski

----------------------------------------
This document contains information on the data and codes necessary to conduct our replication and extension of "The Macroeconomic Eﬀects of Oil Supply News: Evidence
from OPEC announcements," by Diego Känzig. Much of the data and code comes directly from Diego Känzig's original replication package which can be found at https://www.openicpsr.org/openicpsr/project/122886/version/V1/view. 
There are four main folders in our replication file. The first houses the data for our extension. The Excel files N9190US3m.xls, 
Table_8.1_Nuclear_Energy_Overview.xlsx, and Table_10.1_Renewable_Energy_Production_and_Consumption_by_Source.xlsx contain the raw data 
used for the extension. The file also contains .dta files and an additional Excel file that were used to merge the extended data with the author's data. 
The second main folder is named Kaenzig_replication 2 and contains much of Känzig's original data and codes that are needed to replicate the aspects of the paper we wished to highlight. The main code that conducts our extension and the replication codes are within the codes folder of this folder. The third main folder contains the replication and extension outputs and the last folder holds our original code that helps combine our raw extension data with Känzig's data.

----------------------------------------
#1. Data
----------------------------------------
Data from this replication and extension were either obtained directly from Känzig's paper or from the US Energy Information Administration. The data is monthly and all final data used in the analysis are 
contained in .mat files in either the instrument or data folder with the Kaenzig_replication 2 folder. It should be noted that we did not change any of Känzig's variables and the description 
of our data used for the extension is below. We also show how we transformed these variables for the analysis.

USGAS: Monthly US natural gas wellhead price (Dollars per Thousands Cubic Feet). This variable was not transformed.

BIOMASSCONSUMP: Monthly total biomass energy consumption (Trillion Btu). Transformations include taking the log and multiplying it by 100 and second differencing. 

BIOMASSPROD: Monthly total biomass energy production (Trillion Btu). Transformations include taking the log and multiplying it by 100 and second differencing. 

GEOTHERMAL: Monthly geothermal energy consumption (Trillion Btu). Transformations include first differencing.

HYDRO: Monthly hydroelectric energy consumption (Trillion Btu). Transformations include taking the log and multiplying it by 100

NUCLEAR: Monthly nuclear electricity net generation (Million Kilowatthours). Transformations include taking the log and multiplying it by 100 and second differencing.

WIND: Monthly wind energy consumption (Trillion Btu). Transformations include first differencing.

SOLAR: Monthly solar energy consumption (Trillion Btu). Transformations include second differencing.

----------------------------------------
#2. Replication
----------------------------------------
Matlab, R, and Stata are required to extend and replicate the paper. The code that helps combine Känzig's original data with the data from our extension is written in R and Stata. This code can be found in the Replication Code (R/Stata) folder.
From there, Claude was used to convert an excel file with the merged dataset into eight separate .mat files that each contain all of the variables from Känzig's baseline model and 
one of the eight variables used in the extension. The rest of the analysis is completed in Matlab and the codes can be found in within the Kaenzig_replication 2 folder in the code folder. 
Each code and what it produces is listed below.

Projectdataconvert.R: Converts Känzig's baseline monthly dataset to a .dta file to be used in Stata

ECON523Project.do: Merges extension data with baseline monthly data

projectextension.m: Produces our extension results

s03_figures3_5.m: Replicates Figures 3 and 5 from Känzig's paper

s03_figure4a.m: Replicates Figure 4A from the paper

s03_figure4b.m: Replicates Figure 4B from the paper

s03_figure6_8_9a_10_11.m: Replicates Figures 6, 8, 9A, 10, and 11 from Känzig's paper




