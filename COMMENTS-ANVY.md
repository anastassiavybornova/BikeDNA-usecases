**Config file**

* config about true_geometries/centerline: what would it mean if i have true ofr false in each row, what does it refer to?
* bidirectional: True or False should be: ... or string
* can't ref_infrastructure_type be also a column, rather than a dict?
* in reference input requirements the descriptions are different than in the config file
* config file read-in function assumes that all "ref data" specs are filled out, even if we have not ref data available
* Config: What is the difference between "study area name" and "area name"?

**01a**

* debugging is hard! e.g. no "cycleway_both" tags for the study area in OSM >> hard to find out what needs to be changed (commented out in config file but how can one know in advance? better issue tracking OR: make it conditional on whether each of the tags is present...?)

**01b**

* if no incompatible tags >> should be no attempt to plot, put an if statement around it (same for tagging combinations i guess)
* intersection issue check: if no "tunnel" or no "bridge" tags at all present in the OSM data set the code throws an error > make this conditional on tag presence?

**general**

* update geopandas, osmnx, etc. and rerun everything? OR docker image
* percentage of cells reached: should be normed to max number of cells with components, rather than to 100%?

