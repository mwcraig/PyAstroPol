---
title: 'PyAstroPol : A Python package for the instrumental polarization analysis of the astronomical optics.'

tags:
  - Python
  - Astronomy
  - Polarization
  - Optics

authors:
  - name: Hemanth Pruthvi.
    orcid: 0000-0002-4892-6561
    affiliation: "1"

affiliations:
 - name: Leibniz-institut für Sonnenphysik, Freiburg, Germany.
   index: 1

date: 20 August 2020

bibliography: paper.bib
---

# Summary

Polarization analysis is one of the key aspects of optical system analysis in astronomy (). `PyAstroPol` package is meant to provide a means to analyze the polarization properties of a given optical system with relative ease and very limited dependencies. The one simple goal is to calculate the Mueller matrix of a given optical system.

It can be easily distributed along with polarization calibration routines. It incorporates commonly used optics in astronomy such as off-axis mirrors, mirrors with central hole, astronomical source that can be placed by using its declination and hour angle and multi-layer coatings. Albeit there are several limitations, these features should cover a large set of polarization analysis related applications. The salient features and limitations are listed below.

Important Limitations : 
* All the analysis uses strictly ray treatment. Hence, all the limitations of the rays optics are to be born in mind.
* Only circular optics (apertures) can be devised at the moment. Elliptical and rectangular optics are not possible.
* Incidentally, birefringent components are not included yet. The justification for this choice is that behavior of the birefringent components is fairly straight forward as they strongly polarize the light. Hence, they have been given lesser priority.
* Visualization features are limited as the goal of this package is to make it as simple as possible. Hence, widely used `matplotlib` package is used for graphics. All the optics, rays, directions of the coordinate system can be displayed but pan and zoom features are severely limited.
* The package can be described as collection of the important objects used in optics. It is neither interactive nor design-oriented. It means that user must know optical system beforehand, and every time a parameter changes, user must manually rerun the analysis. However, it should be possible to automate it with a little effort. 

Salient features :
* Calculation of Mueller matrix of the given optical system, which is a simple and only end goal. All the rest are by-products of such analysis. However, a major caveat here is that the optical system will be assumed as imaging system i.e., to compute Mueller matrix the electric fields of all the rays will be added coherently after propagating through the system. It implies that the system is imaging type, which is commonplace in astronomy. 
* Astronomical source can be placed directly, using relevant coordinates namely declination, hour angle and latitude of the site.
* Analysis of off-axis components, as they have a significant effect on polarization.
* Effect of multi-layered coatings such as oxide layers and protective coatings on polarization, which are common in astronomical optics.
* All the data such as points of incidence, polarization directions, complex electric field values and more are readily available to the user for any further analysis.
* Material refractive index information can be directly downloaded from popular online source [https://refractiveindex.info/](https://refractiveindex.info/), and used in the applications.
* Spot diagram is possible at any instance, as a by-product of ray tracing. 


# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References