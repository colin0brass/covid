# covid
This is a dashboard for Covid-19 case data, using python and a Jupyter notebook to analyse and display the data from Johns Hopkins University.

Analysis is done using Altair visualisation library, and automatically saved to powerpoint file.

# Setup information
The following were the steps used for first time setup on Mac.

```
## first time setup
cd <directory path>
conda create -n py3 python=3.7
conda activate py3

# jupyter notebook
conda install nb_conda

# altair for data visualisation
pip install altair vega_datasets

# dependencies for notebook
pip install matplotlib seaborn datetime
pip install python-pptx
pip install pycountry_convert

# Altair saver to save charts as files for slide creation
# https://github.com/altair-viz/altair_saver
pip install altair_saver

# altair_saver has dependencies which aren't so straightforward, at least on Mac
# https://www.swtestacademy.com/install-chrome-driver-on-mac/
# choose appropriate zip from files ending "linx64" or "mac64" or "mac_arm64" or "win32"
chromedriver_latest_stable_release='106.0.5249.61'
chromedriver_name=chromedriver_mac_arm64
wget https://chromedriver.storage.googleapis.com/${chromedriver_latest_stable_release}/${chromedriver_name}.zip
unzip ${chromedriver_name}.zip
rm ${chromedriver_name}.zip
mv chromedriver /usr/local/bin/

# load jupyter notebook
# note, might need to ensure Jupyter notebook has correct python kernel selected first time
jupyter notebook covid.ipynb
```


# Startup on subsequent runs
After first-time setup, subsequent runs can simply use the following:
```
cd <directory path>
conda activate py3

# load jupyter notebook
jupyter notebook covid.ipynb
```
