# Software Installation
To get the most out of this workshop, please bring a laptop computer with Python installed.  
We will use **Miniforge** to install Python and all required packages in a clean, reproducible environment.

The following instructions will guide you through installing Miniforge and setting up a `wahgs2026` environment for the workshop.

---

## Part 1 — Install Miniforge

1. Go to the Miniforge website and download the installer for your platform:  
   https://github.com/conda-forge/miniforge

2. Run the installer program you downloaded.  
   - On Windows, the installer is typically named:  
     `Miniforge3-Windows-x86_64.exe`

3. Click through the installer options:
   - Select **“Just Me (recommended)”** if prompted  
   - Default options are fine  
   - **Important:** Choose an installation path **without spaces or special characters**

4. After installation:
   - On Windows, you should see **Miniforge Prompt** in the Start menu  
   - On macOS/Linux, open a terminal

---

## Part 2 — Create the Environment File

We will use an environment file to install Python and all required packages for the workshop.

1. Open a text editor (e.g., Notepad, Notepad++, VS Code)

2. Create a file named: `environment.yml`.  **Windows users:** Make sure the file is not saved as `environment.yml.txt`.

3. Paste the following contents into the file:

```yaml
name: wahgs2026
channels:
  - conda-forge
  - defaults
dependencies:
  - python=3.12
  - flopy
  - jupyterlab
  - scipy
  - geopandas
  - rasterio
  - xarray
  - rioxarray
  - netcdf4
  - git
```

4. Save this file somewhere easy to access (e.g., your home directory)

## Part 3 — Create the Workshop Environment

1. Open the Miniforge Prompt (Windows) or a terminal (macOS/Linux)

2. Run the following command to create the environment.  Be sure to replace `<path-to-file>` with the location where you saved the file.

```
conda env create --file <path-to-file>/environment.yml
```

3. Activate the environment:

```
conda activate wahgs2026
```

4. Your prompt should now look something like:

```
(wahgs2026) C:\Users\YourName>`
```

## Part 4 — Verify Installation

To confirm everything is working:

```
jupyter lab
```

This should open **JupyterLab** in your default web browser.

If it opens successfully in a web browser, you are ready for the workshop.  If it does not open successfully, contact the course instructor.