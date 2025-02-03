<!--
*** Thanks for checking out this README Template. If you have a suggestion that would
*** make this better, please fork the repo and create a pull request or simply open
*** an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->





<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->


<!-- PROJECT LOGO -->
<br />
<p align="center">
  


  <h3 align="center"Tool that allows generating clustering models to characterize household electricity consumption profiles. It includes an implementation of the k-ISAC algorithm, an algorithm for determining the optimal number of clusters by analyzing two curves with quality indicators of the clustering models (the MAE curve of the models, and the curve with the number of small clusters that has each model) </h3>

***Methodology (graphical abstract)***
<img width="845" alt="Captura de pantalla 2023-11-30 a las 9 24 39" src="https://github.com/ursusdm/consumptionprofiles/assets/68539118/a522fb30-ebc9-4bc2-b25b-c6e53ead6f0f">

***ISAC algorithm***

<img width="797" alt="Captura de pantalla 2023-11-30 a las 9 24 54" src="https://github.com/ursusdm/consumptionprofiles/assets/68539118/082aff04-66fe-477e-bad1-953e001784bb">

***Example of a model that characterizes the consumption profiles of a city in Spain***
<img width="814" alt="Captura de pantalla 2023-11-30 a las 9 57 04" src="https://github.com/ursusdm/consumptionprofiles/assets/68539118/a1ab9f2f-7b01-4ccb-836f-7afde5d7e834">

<!-- ABOUT THE PROJECT -->
## About the project

URSUS_CONSUMPTION_PROFILES is a script that implements a methodology to characterize the domestic electricity consumption profiles of any city using clustering algorithms and a new algorithm (k_ISAC_TLP) that allows determining the optimal number of clusters that best represents the consumption profiles.

For a more detailed description of the  methodology and K_ISAC_TLP algorithm you can read the paper.... (añadir enlace al artículo)

...

### Technologies

* Python
* Pyspark
* Jupyter Notebook
* MLIB
  
 ### Datasets

 Any dataset where each row represents the hourly consumption (24 hours) of the day for any consumer. 
 The datasets that have been used for the publication of the article are private, so they cannot be uploaded to the repository.

  ### Script content
  
  The script implements the following functionalities:
  
  * Generation clustering models using big data k-means algorithm for kMin and kMax values for the number of clusters
  * Calculation the MAE of each model
  * Calculation the number of small cluster of each model (less than 1% of the total observations)
  * Calculation of optimal k-value (best model) analyzing the MAE for each model curve, and the curve with the number of small clusters for each model aplying k-ISAC algorithm. 

### Requirements

In order to run the script without problem, it is necessaryis necessary to have installed:

* Jupyter Notebook (Environment to run script cells). Script has comments on the main functionalities that each code cell implements.
* Python (main script language)
* Pyspark (spark with python)
* MLIB (machine Learning with Spark Library)


### Instalation


1. Clone repo
```sh
git clone  https://github.com/ursusdm/consumptionprofiles.git
```
2. **Open script with jupyter notebook and run cells**


<!-- CONTACT -->
## Contact

José del Campo Ávila  - jcampo@uma.es
</br>
Llanos Mora Lopez  - llanos@uma.es
</br>
Francisco Rodríguez Gómez  - francisco.rdg.gmz@uma.es


## Publications

10.1016/j.engappai.2023.107653


 
## ACKNOWLEDGEMENTS

* This work has been supported by the project RTI2018-095097-BI00 in the 
call for projects I+D+i 2018 from Ministerio de Ciencia, Innovación 𝑦 Universidades, Spain.


