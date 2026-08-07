# TJweather Global-Regional Integrated Numerical Weather Prediction System Dataset (SD3)

This repository contains the official descriptive documentation and tutorial notebooks for the **TJweather Global-Regional Integrated Numerical Weather Prediction System Dataset ** hosted on the **AWS Registry of Open Data**.

TJ-NWP is a next-generation numerical weather prediction system developed by **Tianji Weather** based on the Super Dynamics on Cube (SD3) framework.

---

## 📂 Repository Structure

*   [**`tj-nwp-descriptive-documentation.md`**](tj-nwp-descriptive-documentation.md): The comprehensive documentation of the dataset. It includes:
    *   S3 bucket paths, temporal/spatial coverage, and update frequencies.
    *   Full variable lists (149–153 variables) for regional products and typhoon track data parameters.
    *   Direct links to data subsets and access instructions.
*   [**`get-to-know-a-dataset-tj-nwp.ipynb`**](get-to-know-a-dataset-tj-nwp.ipynb): An AWS Open Data "101-level" starter tutorial notebook. It demonstrates:
    *   Direct cloud-native S3 bucket exploration via unsigned requests (no AWS credentials required).
    *   Lazy loading multidimensional NetCDF4 arrays using `xarray`.
    *   Generating geospatial plots (2m temperature, 10m wind barbs with SLP contours, and forecasted typhoon tracks) using `matplotlib` and `cartopy`.

---

## ⚡ Quick Start

To run the tutorial notebook locally or on AWS SageMaker, follow these instructions:

### 1. Prerequisites
Ensure you have Python 3.9+ installed. We recommend installing the required libraries in a virtual environment:

```bash
pip install xarray h5netcdf matplotlib cartopy s3fs
```

*Note: `cartopy` depends on system-level libraries like `GEOS` and `PROJ`. If you encounter installation issues, consider using `conda` / `mamba`:*
```bash
conda install -c conda-forge xarray h5netcdf matplotlib cartopy s3fs
```

### 2. Run the Notebook
Launch Jupyter Lab or VS Code, open `get-to-know-a-dataset-tj-nwp.ipynb`, and run all cells. The notebook will automatically fetch the sample NetCDF4 files directly from S3.

---

## 🪣 AWS Open Data S3 Access

The dataset is publicly available on Amazon S3 in the `us-west-2` region.

*   **S3 Bucket URL:** `s3://tj-nwp/`
*   **Data Layout:**
    *   Southeast Asia Regional Forecasts: `s3://tj-nwp/southeast-asia/`
    *   Africa Regional Forecasts (includes dust variables): `s3://tj-nwp/africa/`
    *   Typhoon Track Forecasts: `s3://tj-nwp/typhoon-track/`

Access is free and anonymous requests are permitted. 

---

## 📄 License & Citations

### License
This dataset and documentation are licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) License.

### Citations
If you use this dataset in your research or applications, please cite:

> Tianji Weather Science and Technology Company. TianJi Global-Regional Integrated Numerical Weather Prediction System Dataset (TJ-NWP). AWS Open Data Registry. https://registry.opendata.aws/tj-nwp/.
