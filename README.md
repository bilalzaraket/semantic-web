## Copyright
© Bilal ZARAKET
# Crime Representation Application

This repository studies the crime dataset available at: https://catalog.data.gov/dataset/crime-data-from-2020-to-present

This dataset reflects incidents of crime in the City of Los Angeles dating back to 2020. This data is transcribed from original crime reports that are typed on paper and therefore there may be some inaccuracies within the data. Some location fields with missing data are noted as (0°, 0°). Address fields are only provided to the nearest hundred block in order to maintain privacy.

Our repository contains different html documents, each displaying specific fields and aspects of the crime dataset and displaying the data using different diagrams.

### Currently available pages:

- descent-of-victim.html: piechart to represent the descent of the victim
- longlat-scatterplot.html: scatterplot to represent the location distribution ( + hashtable)
- los-angeles-crime-distribution.html: map of los angeles to represent the crime distribution
- number-of-parts.html: piechart that represents the number of parts of the crime
- status-of-crime.html: piechart to represent the different statuses of the crimes
- us-map.html: us map to represent crime distribution
- victim-age.html: histogram to represent the age distribution of victims
- victim-sex: piechart to represent victims' sexes

### Running the application:

To run the application, follow the following steps:

- clone the repository
- download fuseki server following the steps defined in this website: https://jena.apache.org/documentation/fuseki2/
- run the fuseki server using the command ./fuseki-server
- open the web interface of apache jena fuseki and create a dataset `http://localhost:3030/`
- Upload the rdf schema found in `.\rdf-schema\Crime_Data_from_2020_to_Present_csv.ttl`
- run a live server and open index.html
- You can access any of the html pages using the Study aspects and maps tabs
- each html page has the diagram and the SPARQL code used to request the data that constitutes it

The diagrams are displayed using D3 and d3sparql (https://github.com/ktym/d3sparql), in addition to some functions we added to d3sparql.js (crimeLocationsMap)

We also use two TOPOJSON files found in topojson folder, to display the different maps, these files are extracted from:

- https://github.com/datadesk/california-topojson-atlas/tree/master/build/counties/processed/county-level (for LA)
- https://github.com/topojson/us-atlas?tab=readme-ov-file
