# Assessing Light Pollution Impact on Star Visibility Using Satellite Radiance and Hipparcos Star Catalog

## Project Overview
This data science capstone project analyzes how artificial light pollution affects nighttime sky visibility and star counts across the globe. By correlating satellite-based night-light radiance datasets with precise physical stellar brightness parameters, this analysis evaluates exactly how many stars are lost to human eyes due to urban growth and light pollution.

The study directly compares key global urban centers against established astronomical dark-sky preservation sites across India, China, South Africa, Brazil, and Russia.

---

## Datasets Used
*   **ESA Hipparcos Star Catalog**: Astrometric data tracking right ascension (RA), declination (Dec), and visual magnitude (mag) for over 100,000 stars.
*   **NASA VIIRS Nighttime Radiance Raster**: High-resolution global satellite raster data representing nighttime light intensity globally. Radiance values serve as a proxy for light pollution.

> **Note**: Due to the massive size of the VIIRS raster file (~2+ GB), it is not committed directly to this repository. You can download the source dataset using the link provided in the references section below.

---

## Tech Stack & Dependencies
This project is built inside a Python virtual environment utilizing key data manipulation, spatial-raster analysis, and visualization libraries:
*   pandas & numpy — Data preprocessing, filtering, and structural transformation.
*   rasterio — Processing, georeferencing, and indexing pixel values from GeoTIFF rasters.
*   matplotlib & seaborn — Statistical charting, boxplots, and geospatial scatter coordinate maps.

---

## Key Exploratory Data Insights
The workflow generates four main plots tracking comparative visibility metrics:
1.  **Total Stars in Sky Region**: Verifies a stable baseline count by isolating an identical 14° x 14° window size around every city coordinate.
2.  **Visible Stars vs. Light Pollution**: Demonstrates a dramatic drop-off in star counts for metropolitan areas compared to nearby dark sites.
3.  **Radiance vs. Visible Stars Scatter**: Confirms a strict, validated negative correlation between raw surface radiance values and naked-eye sky visibility.
4.  **Country-Wise Distribution Boxplot**: Highlights localized disparities inside national borders between high-intensity industrial centers and dark-sky zones.

---

## Results Summary
*   **Extreme Urban Degradation**: Mega-cities like Moscow and São Paulo exhibit near-total star visibility wipeouts, filtering down to 0 visible stars within our search radius under threshold conditions.
*   **Dark-Sky Preserves**: True dark sites like Lake Baikal and Hanle maintain baseline limiting magnitudes up to 6.5, preserving naked-eye views of dozens of local stars within the sample region.

---

## References & Data Sources
*   [ESA Hipparcos Star Catalog](https://esa.int)
*   [NASA VIIRS Nighttime Radiance Data](https://nasa.gov)
