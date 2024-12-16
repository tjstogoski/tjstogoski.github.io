# [Thomas Stogoski](https://tjstogoski.github.io)

![Portrait](https://tjstogoski.github.io/img/portfolioimage1.jpg)

Hey! I'm Thomas. I work as a technician at [Banshee Reeks Nature Preserve](https://www.loudoun.gov/1277/Banshee-Reeks-Nature-Preserve), where I focus on habitat restoration and promoting biodiversity. I am also a student of the [Earth Data Analytics Professional Graduate Certificate](https://earthlab.colorado.edu/earth-data-analytics-professional-graduate-certificate) through the Earth Lab at University of Colorado Boulder. Using modern Earth data techniques, I hope to look at vegetation changes over time.

### Contact Information
* Email me at tjstog@gmail.com
* GitHub [tjstogoski](https://github.com/tjstogoski)
* LinkedIn [Thomas Stogoski](https://www.linkedin.com/in/thomas-stogoski-2a803b142/)

## Educational Background
* **Virginia Commonwealth University** - Bachelor of Music in Music Performance
* **Northern Virginia Community College**
  * *Additional coursework in Biology, Statistics, and Communications*
* **Coastal Carolina University**
  * *Additional coursework in Ecology, Genetics, Chemistry, Physics, Marine Science, and Geology*

## Projects

### Habitat Suitability of *Tsuga canadensis* (L.) Eastern Hemlock

Eastern hemlock is a member of the Pine family (Pinaceae) native to northeastern and Appalachian regions of North America. It is a slow growing tree that may take 300 years to reach maturity and then may live beyond 900 years. Additionally, the Eastern hemlock is a host for at least <a href="https://nativeplantfinder.nwf.org/Plants/3396" target="_blank">90 species of butterflies and moths</a>. However, the tree's range is expected to decline due to a combination of global climate change and pressure from <a href="https://plants.usda.gov/DocumentLibrary/plantguide/pdf/cs_tsca.pdf" target="_blank">the Asian hemlock woolly adelgid</a>.

This analysis examines the future habitat suitability for Eastern Hemlock under different climate change scenarios within George Washington National Forest and Jefferson National Forest. The sites were chosen because of their continuous range, stretching most of the range of Virginia's Appalachian region. The two climate change scenarios, described in the <a href="https://www.ipcc.ch/site/assets/uploads/2018/04/ipcc_ar5_leaflet.pdf" target="_blank">IPCC Fifth Assessment Report (AR5)</a>, project future greenhouse gas concentrations. RCP 4.5 is described as an intermediate scenario where emissions peak around 2040. RCP describes a scenario where emissions continue to rise throughout the 21st century and is generally the basis of a worst-case climate change scenario.

The analysis employs a fuzzy logic model using a <a href="https://www.mathworks.com/help/fuzzy/gaussmf.html" target="_blank">Gaussian membership function</a> to assign suitability scores between 0 and 1 for raster data of the following variables:
* Soil pH - taken at 30-60 cm in depth and obtained from the <a href="http://hydrology.cee.duke.edu/POLARIS/PROPERTIES/v1.0/" target="_blank">Polaris dataset</a>.
* Topographic slope - derived from elevation data of the SRTMGL1 NASA Shuttle Radar Topography Mission Global 1 arc second V003 dataset through the [earthaccess API](https://github.com/nsidc/earthaccess/).
* Precipitation - from the <a href="http://thredds.northwestknowledge.net:8080/thredds/reacch_climate_CMIP5_macav2_catalog2.html" target="_blank">MACAv2 THREDDS data server</a>. This analysis uses Bei-jing Normal University Earth System Model for projected climate data of the end of the 21st century.

Tolerable variable ranges for *Tsuga canadensis* were obtained from <a href="https://plants.usda.gov/plant-profile/TSCA" target="_blank">USDA Plants Database</a> for Soil pH and Precipitation needs. Optimal values were derived by taking an average of the upper and lower thresholds. Slope preference of *Tsuga canadensis* is described in <a href="https://www.srs.fs.usda.gov/pubs/ja/ja_narayanaraj001.pdf" target="_blank">Narayanaraj, Bolstad, Elliott, and Vose, 2010</a>.

#### Results
![Habitat Suitability of Tsuga canadensis George Washington National Forest under RCP 4.5](img/TSCA_GWNF_RCP45.jpg) ![Habitat Suitability of Tsuga canadensis George Washington National Forest under RCP 8.5](img/TSCA_GWNF_RCP85.jpg)

Though much of George Washington National Forest will remain habitable for *Tsuga canadensis* at the end of the century, a decrease in habitat is expected if emissions continue to rise as described by the RCP 8.5 scenario. However, the Southeastern region of the forest may see an increase in Eastern hemlock, possibly due to a wetter climate.

![Habitat Suitability of Tsuga canadensis Jefferson National Forest under RCP 4.5](img/TSCA_JNF_RCP45.jpg) ![Habitat Suitability of Tsuga canadensis Jefferson National Forest under RCP 8.5](img/TSCA_JNF_RCP85.jpg)

Unfortunately, an error occurred during the processing of the raster layers for Jefferson National Forest, resulting in only the Northeastern tip of the forest being shown. However, we can still see similarity to George Washington National Forest, where overall habitat may decline in quality but Eastern regions may see an increase in available habitat for Eastern hemlock. This will be looked at again when I next revist the project.

**Formal data citations to come**

<a href="https://github.com/tjstogoski/Habitat-Suitability" target="_blank">See the full project here</a>

 
### [50 Years of Temperature Data Show Rising Temperatures at Back Bay National Wildlife Refuge, VA](posts/02-climate/Back_Bay_NWR_climate_analysis.html)
![Back Bay Climate Plot](img/back_bay_NWF_climate_plot.jpg)

From 1954 to 2006, Back Bay NWR has warmed an average of 0.087&deg;C per year. At 0.87&deg;C per decade, this rate of warming is over four times that of the <a href="https://www.climate.gov/news-features/understanding-climate/climate-change-global-temperature" target="_blank">global rate of warming from 1982 to 2023 as calculated by NOAA (0.20&deg;C per decade)</a>. It was interesting to note the period of cooler temperatures observed starting in 1982, which coincided with a <a href="https://psl.noaa.gov/enso/climaterisks/years/top24enso.html" targe="_blank">strong El Nino event</a>. Looking into this also lead me to learn about the <a hre="https://volcano.oregonstate.edu/el-chichon-mexico-1982" target="_blank">El Chichon volcanic eruption of 1982</a>, which also likely contributed to cooler temperatures, as the aerosol sulfur dioxide emitted from the eruption reflects solar radiation.
[See the full post here](posts/02-climate/Back_Bay_NWR_climate_analysis.html)

### Map of Banshee Reeks Nature Preserve

Banshee Reeks Nature Preserve (BRNP) protects 695 acres of the Northern Virginia Piedmont through a conservation easement held by the Virginia Outdoors Foundation. It is managed by the Department of Parks, Recreation & Community Services of Loudoun County, Virginia, USA. The map shows the forests, fields, wetlands, and waters that make up the preserve and serve to teach us of the natural and cultural resources of the region.

<embed type="text/html" src="img/brnp_map.html" width="600" height="600">
