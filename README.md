# Nighttime Light Data (NLD) Analysis

This script is designed for preprocessing Satellite Nighttime Light Data using ArcGIS. It performs several tasks to prepare the data for further studies. The preprocessed Satellite NLD can be used in various studies, including urban economics, crisis tracking, development economics research and natural disaster analysis.

## Datasets
- Satellite Nighttime Light Data downloaded from Earth Observation Group website, Payne Institute for Public Policy, Colorado School of Mines (https://eogdata.mines.edu/products/dmsp/). DMSP data collected by US Air Force Weather Agency.
- Country boundary shapefile is downloaded from https://gadm.org/

## Instructions
1. **Clip NLD Data using Country Shapefile**
   - Input: Nighttime Light Data in raster format
   - Process: Extract by Mask using country boundary
   - Output: Raster for the specific region
    
2. **Convert NLD Raster to Polygon**
   - Input: Clipped Nighttime Light Data
   - Process: Convert raster to polygon
   - Output: Polygon feature class

3. **Clip Grid to Country Shape**
   - Input: Shapefile, NLD Polygon
   - Process: Clip grid to the country shape
   - Output: Clipped grid feature class 

4. **Calculate Zonal Statistics of each pixel/region**
   - Input: Shape file, NLD raster
   - Process: Calculate zonal statistics (mean, min, max, range, etc) for each grid cell
   - Output: Zonal statistics table for each satellite-year

## Notes
- Modify the file paths and run the script in ArcGIS environment.
- Adjust the parameters based on the specific requirements of your analysis.
