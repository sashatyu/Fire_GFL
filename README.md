This is a project providing equations, code and input data to compute the area of forest loss due to fire and estimate accuracy of the resulting map in the following study: Tyukavina et al. (in review) "Global trends of forest loss due to fire, 2001-2019". For a detailed description of the study please refer to the publicaiton.

Project files:
* Equations.docx - Equations from the Supplementary Information of Tyukavina et al. article
* Compute_area_and_accuracy.ipynb - Python 3 code implementing the equations
* Strata_info.txt - sampling design information 

   Columns: 
   * "Region" - Unique region name, for region boundaries please refer to the article
   * "Stratum" - Stratum ID (1-N)
   * "Area_km2" - Stratum area
   * "Sample size" - Number of pixels sampled in each stratum
* Sample_data.txt - input data for each sample pixel

   Columns:
   * "ID" - Unique sample pixel ID (1-n)
   * "Region" - Unique region name, for region boundaries please refer to the article
   * "Stratum" - Stratum ID (1-N)
   * "Reference" - Reference sample value, 1 if sample pixel was identified as forest loss due to fire during the validation process, and 0 otherwise
   * "Pixarea" - Area of pixel in km2
   * "Map" - Map value from the map adjusted to match sample-based estimate, with 1 corresponding to forest loss due to fire, and 0 - to forest loss due to other drivers. This is the version of the map used for area and trend reporting in the paper, where any forest loss within year 2000 zero % tree canopy cover (Hansen et al. 2013) is mapped as "forest loss due to other drivers".
