# Soil Nutrient analysis

## Objectives:
* To create a smart computer program using machine learning that can tell us about the nutrients in the soil by using SCROPAN model. This will help farmers know how to take care of their land better for growing crops.
* To empower farmers to make decisions for sustainable crop production and soil management, we leverage machine learning to enhance soil nutrient prediction.
* To significantly impact agriculture and related industries, the project focuses on accurately predicting soil nutrient levels. This provides valuable insights for advancing agricultural practices and ultimately boosting crop productivity.

## Team members:
* Deep Pethani : https://github.com/deeppethani02
* Harsh Chothani : https://github.com/Harsh-Chothani
* Darshan Gajera : https://github.com/Darshan5G
* Jasmin Babariya : https://github.com/Jasminbabariya48

## Data:
1. Study area : Vadodara(Baroda) District of Gujarat, India
2. Normalized Difference Vegetation Index (NDVI) : [Google Earth Engine](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_32DAY_NDVI)
3. Digital Elevation Model (DEM) : [Google Earth Engine](https://developers.google.com/earth-engine/datasets/catalog/USGS_SRTMGL1_003)
4. Land Surface Temperature (LST) : [Google Earth Engine](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_TOA)
5. Ground data : By Anand Agricultural University (AAU)
6. Baroda District Shape(.shp) file

## Install required packages:
~~~
!pip install rasterio
!pip install matplotlib
~~~

## Procedure:
1. Download the main folder named Soil_nutrient_analysis and extract it.
2. Download folder containing [satellite image](https://drive.google.com/drive/folders/1l2i0mE7PCISoPE8SN8OCFxJhA5h-IriT?usp=sharing) by clicking on it, extract the folder from zip and move it in the folder extracted previously.
2. Open the raster image file and extract bands 1, 2, and 3. 
2. Display each band as a separate raster image. 
3. Prepare the training data by reshaping the band data and creating a pandas DataFrame. 
4. Train a Linear Regression model using the training dataset. 
5. Save the trained model to a file. 
6. Load the raster image file and extract bands 1, 2, and 3. 
7. Reshape the band data and normalize the bands using MinMaxScaler. 
8. Make predictions on the normalized data using the trained model. 
9. Save the predicted values to a pandas DataFrame. 
10. Create a new raster image for regression with the predicted values. 
11. Evaluate the model on the test set and print the RMSE and MAE values.

## Assumptions:
The code assumes that the input raster image has three bands (NDVI, DEM, and LST) and the training dataset contains a single column for prediction (K20_kg_ha_). You may need to modify the code to suit your specific dataset and raster image structure.

## Referances:
* Khosravani, M., Moosavi A. A., & FallahShamsi S. R. (2023). Digital mapping to exfrapolate the selected soil fertility attributes in calcareous soils ofa semiarid region in Iran. Journal of Soils and Sediments, 1-23.
* Wu, Z., Chen, Y, Zhu, Y., Feng, X., Qu, J., Li, G., ... & Yan, Q. (2023). Mapping Soil Organic Carbon in Floodplain Fannland: Implications of Effective Range of Environmental Variables. Land, 12(6), 1198.
* [Rasterio Documentation](https://buildmedia.readthedocs.org/media/pdf/rasterio/latest/rasterio.pdf)
