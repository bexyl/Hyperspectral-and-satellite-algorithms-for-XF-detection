## Data and codes for the release of hyperspectral algorithms to high-resolution multispectral satellites for detecting <i>Xylella fastidiosa</i> infections

### ACHIEVEMENT
We developed a feature–weighted machine learning framework, was developed combining random forest and partial least squares discriminant analysis, to distinguish and prioritize spectral traits indicative of biotic or abiotic stress. Models were trained on a comprehensive dataset spanning different species (notably almond and olive), two major vascular pathogens (<i>Xylella fastidiosa</i> and <i>Verticillium dahliae</i>), and a range of water stress levels, selected because of their overlapping spectral signatures. The framework integrates narrow–band hyperspectral indices (sensitive to pigments, water content, and structural properties) with plant traits derived from radiative transfer model inversion (e.g., chlorophyll, carotenoids, anthocyanins, water content, LAI, LIDF).
Trait and index importance were analysed to identify the features most effective in discriminating between biotic and abiotic stress. Models were validated across species and pathogens, with performance evaluated using overall accuracy (OA) and Cohen’s kappa (κ). Using large–scale airborne hyperspectral imaging, the framework achieved detection accuracies exceeding 92% while reducing uncertainty in pathogen detection to below 6%.<br>
Building on this foundation, the approach was transferred to high–resolution commercial satellite multispectral imagery (WorldView-2 and -3) and directly compared with airborne hyperspectral and thermal imaging data. Satellite imagery proved effective for detecting intermediate and advanced <i>X. fastidiosa</i> symptom infections (OA 0.63–0.83, κ 0.29–0.68), though early detection was limited by the inability of multispectral sensors to capture key plant traits and subtle physiological changes. In contrast, airborne hyperspectral imaging maintained high accuracy for early detection, reinforcing the importance of spectral and trait resolution in operational disease surveillance.<br>
The algorithms were developed by scientists at the University of Melbourne (Australia), and subsequently validated at IAS–CSIC (Spain), ensuring both methodological rigor and applicability under real agricultural contexts.

### INSTRUCTIONS
The datasets provided in this repository are detailed as follows:

| Dataset | Download  | Description |
| ------------- |:-----------------| -----|
|Biotic-<i>Xf-</i>infected olive| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Biotic-Xf-infected%20olive">Biotic-<i>Xf-</i>infected olive</a>  | Airborne and field evaluation data collected during 2016-2017 in Apulia, Italy<sup>*</sup>| 
|Biotic-<i>Xf-</i>infected almond| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Biotic-Xf-infected%20almond/">Biotic-<i>Xf-</i>infected almond</a>  | Airborne and field evaluation data collected during 2019 in Majorca, Spain<sup>*</sup> | 
|Biotic-<i>Vd-</i>infected olive| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Biotic-Vd-infected%20olive/">Biotic-<i>Vd-</i>infected olive</a> | Airborne and field evaluation data collected during 2011 in Castro del Rio, Spain<sup>*</sup>  | 
|Abiotic-water-stress-olive| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Abiotic-water-stress-olive/">Abiotic-water-stress-olive</a> | Airborne and field evaluation data collected during 2016 and 2017 in Cordoba, Spain<sup>**</sup>  | 
|Abiotic-water-stress-almond| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Abiotic-water-stress-almond/">Abiotic-water-stress-almond</a> | Airborne and field evaluation data collected during 2016 and 2017 in Cordoba, Spain<sup>**</sup> | 
|Biotic-<i>Xf-</i>qPCR olive| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Biotic-Xf-qPCR%20olive/">Biotic-<i>Xf-</i>qPCR olive</a> | Airborne,  field evaluation and qPCR data collected in Apulia, Italy<sup>***</sup>  | 
| Biotic-<i>Xf-</i>qPCR almond| <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Biotic-Xf-qPCR%20almond/">Biotic-<i>Xf-</i>qPCR almond</a>| Airborne,  field evaluation and qPCR collected in Majorca, Spain<sup>***</sup> | 


<sup>* Databases containing Disease severity (SEV), plant traits estimated by model inversion and spectral indices calculated from the hyperspectral and thermal imagery </sup> <br>
<sup>**  Databases containing plant traits estimated by model inversion and spectral indices calculated from the hyperspectral and thermal imagery </sup> <br>
<sup>*** Databases containing Disease severity (SEV), plant traits estimated by model inversion and spectral indices calculated from the hyperspectral and thermal imagery, and qPCR data</sup>

The R codes provided in this repository are detailed as follows:

| Code | Download  | Description |
| ------------- |:-----------------| -----|
|<li> Feature-weighted Random Forest </li> <li> Unsupervised reclassification </li>|  <a href="https://github.com/bexyl/Hyperspectral-and-satellite-algorithms-for-XF-detection/blob/main/Codes/"></i>Codes</a> |  <li> Feature weighted Random forest algorithm including the feature importance into the models </li> <li> Spectral clustering algorithm that uses divergent-specific biotic and abiotic spectral traits </li>  |

The feature weighted Random forest algorithm includes the feature importance for the disease prediction into the model <br>
The spectral clustering algorithm is used in the reclassification stage in order to reclassify the "uncertain" trees using the divergent-specific biotic and abiotic spectral traits. 


### Packages requirements

<ul>
  
 <li> These algorithms were implemented in R (v. 3.5.3; R Development Core Team, Vienna, Austria)</li>
  
<li> The code for the leaf measurements analysis requires the following packages: "RColorBrewer", "ggplot2", "gridExtra", "dplyr" and "grid"  </li>
  
<li> The feature weighted random forest algorithm is included in the R package “viRandomForests” proposed by Liu, Y. & Zhao, H (2017) <sup>* </li>
  
<li>The “viRandomForests” package could be obtained from: <a href="http://zhaocenter.org/softwares/">“viRandomForests” R package </a>  </li>

<li> The unsupervised spectral clustering algorithm requires the kernlab package <sup>** </li>  
  
<li> Both algorithms require the Caret Package <sup>*** </li>    
 </ul> 



<sup>*</sup> Liu, Y. & Zhao, H. Variable importance-weighted random forests. Quant Biol 5, 338–351 (2017) <br>

<sup>**</sup> Karatzoglou, A., Smola, A., Hornik, K. & Zeileis, A. kernlab An S4 Package for Kernel Methods in R Journal of Statistical Software 11, 1–20 (2004); https://CRAN.R-project.org/package=kernlab <br>


<sup>***</sup> Kuhn, M. et al. caret: Classification and Regression Training v6.0-78 
(CRAN, 2017); https://CRAN.R-project.org/package=caret  <br>



### Contact information

Prof. Pablo J. Zarco-Tejada
<br>email: pablo.zarco@csic.es
<br>https://blogs.unimelb.edu.au/hypersens/
<br>http://quantalab.ias.csic.es/
