# Water Level Prediction for USGS Gage Sites

## Project Overview
This project aims to predict water levels across 10 specific USGS gage sites using machine learning models. The data is sourced from USGS and VIMS (Virginia Institute of Marine Science) cameras capturing images of water levels under various environmental conditions. This work involves preprocessing images, training predictive models, and evaluating performance to improve water level monitoring and prediction accuracy.

---

## Sites and Data Summary

| #  | USGS Gage ID   | Location                                | State | Training Date Range       | Prediction Date Range    | Frequency (mins) | Notes                                                                                                 | Camera URL                                                                 |
|----|----------------|-----------------------------------------|-------|---------------------------|--------------------------|------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1  | 0204295505     | VA_Pinewood_Virginia_Beach             | VA    | 10/01/2021 - 12/31/2021   | 01/01/2022 - 01/30/2022  | 6                | Staff gage within 25 ft; ideal for tidal creek site.                                                 | [Link](https://apps.usgs.gov/sstl/camera/0204295505_VA_Pinewood_Virginia_Beach) |
| 2  | 08051100       | TX_Ray_Roberts_Lake                    | TX    | 12/01/2021 - 12/31/2021   | 01/01/2022 - 04/30/2022  | 15               | Staff gage close to camera; non-tidal lake.                                                          | [Link](https://apps.usgs.gov/hivis/camera/TX_Ray_Roberts_Lake)               |
| 3  | 01437500       | NY_Neversink_Goddefroy                 | NY    | 12/01/2023 - 12/31/2023   | 12/01/2024 - 12/31/2024  | 15               | Bright street lamp affects night IR imagery; non-tidal site.                                         | [Link](https://apps.usgs.gov/hivis/camera/NY_Neversink_Goddefroy)            |
| 4  | 0167300055     | Mechumps Creek at Hill Carter Parkway  | VA    | 07/13/2022 - 07/31/2022   | 08/01/2022 - 11/30/2022  | 15               | Camera high above flooded areas; non-tidal riverine tributary.                                       | [Link](https://apps.usgs.gov/hivis/camera/VA_Mechumps_Creek_at_Hill_Carter_Parkway_at_Ashland) |
| 5  | 05427965       | Spring Harbor Storm Sewer OVERVIEW     | WI    | 05/01/2024 - 06/01/2024   | 06/01/2024 - 07/01/2024  | 60/5            | Minimal adverse weather impact; records every 5 mins when water > 2 ft.                              | [Link](https://apps.usgs.gov/sstl/camera/05427965_Spring_Harbor_Overview)    |
| 6  | 05335450       | North Fork Clam River                 | WI    | 09/15/2023 - 10/15/2023   | 05/01/2024 - 06/01/2024  | 60               | Vertical plate within 15 ft of camera; ideal non-tidal site.                                         | [Link](https://apps.usgs.gov/hivis/camera/WI_North_Fork_Clam_River_near_Siren) |
| 7  | 02169500       | Congaree River at Columbia             | SC    | 01/01/2024 - 01/31/2024   | 05/01/2024 - 05/31/2024  | 15               | Images available from 9 AM to 8 PM daily; non-tidal riverine sensor.                                 | [Link](https://apps.usgs.gov/hivis/camera/SC_Congaree_River_at_Columbia)     |
| 8  | 11447650       | Sacramento River at Freeport           | CA    | 05/24/2024 - 06/24/2024   | 07/01/2024 - 08/01/2024  | 60               | Staff gage within 25 ft; tidal creek site.                                                           | [Link](https://apps.usgs.gov/hivis/camera/CA_Sacramento_River_at_Freeport)   |
| 9  | 021720677      | Cooper River at Filbin Creek           | SC    | 04/03/2024 - 04/21/2024   | 05/01/2024 - 06/30/2024  | 15               | Images from 9 AM to 8 PM; bridge piling ~150 ft from camera; tidal river inlet.                      | [Link](https://apps.usgs.gov/hivis/camera/SC_Cooper_River_at_Filbin_Creek_at_North_Charleston) |
| 10 | 0214668150     | McMullen Creek at Lincrest Place       | NC    | 01/01/2024 - 01/31/2024   | 02/01/2024 - 05/31/2024  | 5                | No night vision or staff plate; frequent flooding over roadway during daytime.                       | [Link](https://apps.usgs.gov/hivis/camera/NC_McMullen_Creek_at_Lincrest_Place_at_Charlotte)   |

---

## Methodology
### 1. **Data Collection**
- Extract images and metadata from the listed URLs for the specified time ranges.
- Preprocess images to normalize and align water level markers.

### 2. **Model Training**
- Use training datasets to train machine learning models (e.g., CNNs or custom image classifiers).
- Incorporate time-series data and image recognition for improved accuracy.

### 3. **Prediction**
- Apply the trained models to prediction datasets.
- Validate predictions using ground truth water level measurements.

### 4. **Evaluation**
- Evaluate model performance using metrics such as Mean Absolute Error (MAE) and RMSE.
- Analyze predictions for accuracy and consistency.

---

## Applications
- **Flood Monitoring**: Early warnings for potential flooding events.
- **Water Resource Management**: Optimize water usage in rivers, lakes, and reservoirs.
- **Environmental Analysis**: Understand patterns in water levels due to climate change.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
