# 🌍 Clip Multiple IMG Rasters with a Shapefile in R 🌿

Welcome to the **IMG Raster Clipper**! 🎉 This R script simplifies clipping multiple `.IMG` raster files using a shapefile, ensuring **maximum inclusivity** by leveraging coverage fractions. Ideal for geospatial analysts working with satellite imagery, GIS data, or environmental datasets! 🗺️

---

## 🚀 What Does This Script Do?

This script automates clipping `.IMG` raster files with a shapefile in R, keeping pixels with any coverage. Here's the workflow:

1. 📂 **Prompts you to select** a folder with `.IMG` raster files.
2. 🗺️ **Asks for a shapefile** (`.shp`) to define the clipping boundary.
3. 💾 **Lets you choose an output folder** for saving clipped rasters.
4. 🔄 **Processes each `.IMG` file** by:
   - 📖 Reading the raster and shapefile.
   - 🌐 Aligning Coordinate Reference Systems (CRS) by reprojecting the shapefile if needed.
   - ✂️ Cropping the raster to the shapefile's extent.
   - 🖌️ Rasterizing the shapefile to compute coverage fractions.
   - 🎭 Creating a binary mask to retain pixels with any coverage (>0).
   - 💾 Saving the clipped raster in `.IMG` format (using ENVI filetype).
5. 📊 **Summarizes** processed files and any errors.

The script uses `terra`, `sf`, and `tcltk` packages for geospatial operations and interactive file selection. 🛠️

---

## 📋 Prerequisites

Ensure you have:

- 🖥️ **R installed** (version 4.0 or higher recommended).
- 📦 **Required R packages**:
  - `terra`: For raster and vector processing.
  - `sf`: For shapefile handling.
  - `tcltk`: For interactive dialogs.
- 📁 **Input files**:
  - A folder with `.IMG` raster files (e.g., ERDAS IMAGINE format).
  - A `.shp` shapefile with a valid CRS.
- 💾 **Write permissions** for the output folder.

The script auto-installs missing packages! 🚀

---

## 🛠️ How to Use the Script

1. 📥 **Download the script**:
   - Save `img_raster_clipper.R` to your R working directory.

2. 📂 **Prepare your files**:
   - Store `.IMG` raster files in a folder.
   - Have a valid `.shp` shapefile ready.

3. 🏃 **Run the script**:
   - In R or RStudio, source the script:
     ```R
     source("img_raster_clipper.R")
     ```
   - Or paste the code into the R console.

4. 🖱️ **Follow prompts**:
   - Select the folder with `.IMG` files.
   - Choose the `.shp` shapefile.
   - Pick an output folder for clipped rasters.

5. ✅ **Check results**:
   - Clipped rasters are saved with a `clipped_` prefix in the output folder.
   - A summary reports successful and failed files.

---

## 🎯 Features & Benefits

- **Interactive**: User-friendly prompts for file and folder selection. 🖱️
- **CRS Handling**: Auto-reprojects shapefile to match raster CRS. 🌐
- **Inclusive Clipping**: Retains pixels with any coverage using fractions. 🔲
- **Robust**: Validates shapefile geometries and handles errors gracefully. ⚠️
- **Efficient**: Processes multiple rasters with progress updates. ⏳

---

## ⚠️ Notes & Tips

- **Shapefile Quality**: Ensure your shapefile has valid geometries to avoid issues.
- **CRS Alignment**: Reprojection may increase processing time for large datasets.
- **Output Naming**: Clipped files are prefixed with `clipped_` to prevent overwriting.
- **Performance**: Ensure sufficient memory and disk space for large rasters.
- **Dependencies**: Requires `terra`, `sf`, and `tcltk`. Internet needed for package installation.

---

## 📚 References

- [terra R Package](https://cran.r-project.org/package=terra): For raster and vector operations.
- [sf R Package](https://cran.r-project.org/package=sf): For shapefile handling.
- [tcltk R Package](https://cran.r-project.org/package=tcltk): For interactive dialogs.
- [GeeksforGeeks: Clipping Raster in R](https://www.geeksforgeeks.org/clipping-raster-using-shapefile-in-r/)

---

## 🌟 Contributing

Fork this repository, submit pull requests, or open issues for improvements or bug reports! 🙌 Let's enhance geospatial processing together! 🚀