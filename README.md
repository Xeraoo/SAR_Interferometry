# SAR Interferometry: Induced Seismicity Analysis  
**Authors**: Bartosz Augustyn, Tymoteusz Maj  
**Institution**: AGH University of Science and Technology in Krakow  
**Department**: Mining Geodesy and Environmental Engineering  
**Field of Study**: Remote Sensing and GIS  
**Date**: 2024  

## Project Overview  
This project, titled *"SAR, Interferometry - Project 2 - Induced Seismicity"*, focuses on analyzing ground surface displacements caused by a mining-induced earthquake that occurred on November 29, 2016, at one of KGHM's mining sites in Poland. Leveraging **Differential Interferometric Synthetic Aperture Radar (DInSAR)** techniques, we investigated the extent and progression of surface movements triggered by this seismic event. This work provides valuable insights into the dynamics of induced seismicity and demonstrates the application of advanced remote sensing methods to real-world environmental challenges.

The project combines satellite data processing, interferometric analysis, Python scripting, and geospatial visualization to deliver a comprehensive study of surface displacement, making it a strong showcase of technical proficiency in remote sensing and GIS.

---

## Objectives  
- Quantify ground surface displacements caused by mining-induced seismicity.  
- Apply DInSAR techniques to measure and visualize surface movements over time.  
- Develop a workflow integrating radar data processing, phase unwrapping, and geospatial analysis.  

---

## Technologies and Tools  
- **Satellite Data**: Sentinel-1 SLC (Single Look Complex) radar images from the Copernicus Data Space Ecosystem.  
- **Software**:  
  - SNAP (Sentinel Application Platform) for interferometric processing.  
  - SNAPHU for phase unwrapping.  
  - QGIS for geospatial visualization and contour mapping.  
- **Programming**:  
  - Python (NumPy, Pandas, Matplotlib, SciPy) for data interpolation and visualization.  
  - Rasterio for handling geospatial raster data.  
- **Geospatial Standards**: EPSG:2176 coordinate reference system, WGS84 projection, SRTM 1 Sec HGT digital elevation model.  

---

## Methodology  
The project followed a structured workflow to process Sentinel-1 radar data and derive surface displacement measurements in the Line of Sight (LOS) direction. Below is an overview of the key steps:  

1. **Data Acquisition**  
   - Downloaded Sentinel-1 SLC images for December 8 and December 20, 2019, covering the study area.  

2. **Data Preprocessing**  
   - Performed TOPS splitting, orbit correction, co-registration, and spectral diversity enhancement using SNAP.  

3. **Interferogram Generation**  
   - Created an interferogram and estimated coherence to analyze phase differences.  
   - Applied Goldstein phase filtering and TOPS deburst to refine the data.  

4. **Phase Unwrapping**  
   - Utilized SNAPHU to unwrap the interferometric phase and imported results back into SNAP.  

5. **Displacement Calculation**  
   - Converted unwrapped phase data into metric displacement values using the Phase to Displacement operator.  
   - Applied terrain correction with Range Doppler Terrain Correction.  

6. **Data Refinement**  
   - Created a coherence mask (threshold > 0.3) and applied multilooking to reduce noise.  

7. **Interpolation and Visualization**  
   - Developed a custom Python script to interpolate displacement data and export it as a GeoTIFF.  
   - Visualized results in QGIS with contour lines to highlight displacement patterns.  

---

## Key Deliverables  
- A raster dataset representing surface displacement in meters, visualized as a subsidence map.  
- Contour lines generated in QGIS to illustrate displacement gradients.  
- A Python script for interpolating and plotting geospatial data, demonstrating programming skills.  

---

## Results  
The analysis successfully mapped surface displacements caused by the 2016 mining-induced earthquake, revealing the spatial extent and magnitude of ground movements. The combination of DInSAR processing and geospatial tools provided a clear picture of subsidence patterns, validated by high-coherence areas in the interferogram. This project highlights the potential of SAR interferometry for monitoring environmental impacts in mining regions.

![image](https://github.com/user-attachments/assets/d02612ae-85a5-4fd7-aae3-0bf7ffc63aeb)


---

## Skills Demonstrated  
- **Remote Sensing**: Proficiency in SAR data processing and DInSAR techniques.  
- **Geospatial Analysis**: Expertise in terrain correction, coordinate systems, and GIS visualization.  
- **Programming**: Ability to write and apply Python scripts for scientific data analysis.  
- **Problem Solving**: Handling complex workflows from raw satellite data to actionable insights.  

---

## Future Applications  
This methodology can be adapted to monitor other seismically active regions or industrial sites, offering a scalable approach to studying ground deformation. Potential enhancements include automating the pipeline with Python or integrating real-time Sentinel-1 data feeds.

---
