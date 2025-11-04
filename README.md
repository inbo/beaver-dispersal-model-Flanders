# Beaver dispersal model (Flanders)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17406546.svg)](https://doi.org/10.5281/zenodo.17406546)

This GitHub repository provides the source code for a species distribution model created for European beaver in Flanders. This model is an improved version of the model described in the paper by [Huysentruyt & Rutten (2024)](https://doi.org/10.1007/s10344-024-01831-1) in the European Journal of Wildlife Research.

This code models how beavers disperse in Flanders. The model code is presented in [Beaver_dispersal_model_Flanders.Rmd](Beaver_dispersal_model_Flanders.Rmd).

As starting points for dispersal we used a layer with 457 known territories of beavers in Flanders, represented by point locations and provided as a shapefile ([Input/Beaver_territories_2024.shp](Input/Beaver_territories_2024.shp)). The model uses a few key layers to simulate beaver movement:

* Habitat Suitability: A raster layer created by a Maxent model that shows suitable beaver habitats in Flanders and a 10 km buffer around it ([Input/projection_wide.tif](Input/projection_wide.tif)).
* River Systems: A linestring layer representing the major rivers in the same area. This is combined with the habitat suitability layer ([Input/Shape_RIV.shp](Input/Shape_RIV.shp)).
* Grid: An UTM 1x1 km square layer of Flanders. This layer is used to project the final output of the dispersal model, making it easier to visualize and analyze the results ([Input/Vlaanderen_UTM.shp](Input/Vlaanderen_UTM.shp)).

The code’s goal is to predict and map where beavers might move based on these habitat and river data sets.
