Ppaers codes for "Global long-term daily 1km surface soil moisture dataset with physics-informed machine learning (GSSM1km)".
Global Surface Soil Moisture (GSSM1km) is a global surface soil moisture (0-5 cm) at 1 km spatial and daily temporal resolution over the period 2000-2020. The data is generated using a machine-learning based trained with in-situ soil moisture measurement from more than 1000 stations mostly from the International Soil Moisture Network (ISMN) website.

To reproduce GSSM1km using the code files in this repository. Code files are as follows:
(1) TI generation is used for getting Topographic Index, but this data is public already.
(2) GSSM1km generation is the most important code file, which include the whole process of how to preprocess the predictors and train the model. The code GSSM1km generation is for Europe, you can change the variable EuropeBoundary in line 13 to run other places.
(3) For the continuous LST in other places, you need to run the codes from Shiff to fill in the gaps (https://github.com/shilosh/ContinuousLST)
Shiff, S., Helman, D. & Lensky, I. M. Worldwide continuous gap-filled MODIS land surface temperature dataset. Scientific Data 8, 1-10 (2021).

Some processed data needed are public. If you run my code (GSSM1km generation), it will automatically access them. 

The list of these processed data are as follows:
(1)The training and testing samples: https://code.earthengine.google.com/?asset=users/qianrswaterr/GlobalSSM2022/trainTestFinal2022-0509coor;
https://code.earthengine.google.com/?asset=users/qianrswaterr/NLsamples/trainTestNL2022-0509coor
(2)The validating evaluating samples: https://code.earthengine.google.com/?asset=users/qianrswaterr/GlobalSSM2022/valiEvaFinal2022-0509coor
(3)Topographic Index (TI): https://code.earthengine.google.com/?asset=users/qianrswaterr/GlobalSSM/TIele1000resample0709
(4)Depth To Bedrock (DTB): https://code.earthengine.google.com/?asset=users/qianrswaterr/predictors/BDTICM_M_1km_ll
(5)Water Table Depth (WTD): https://code.earthengine.google.com/?asset=users/qianrswaterr/WTD
(6)Continuous LST in Europe from 2012 to 2020: https://code.earthengine.google.com/?asset=users/qianrswaterAmerica/LSTEuropeMOD11A1


