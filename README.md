# gpxprocessing #

Process GPX files - at first one script but who knows?

## preprocessGPXtracks ##

A script that takes a gpx file and copies it, writing a new track
around every segment, changing the track name of each track to the
date time of the first trackpoint, and deleting tracks with 3
trackpoints or less (see minpoints option). With the --crop option, it
can also drop each first and last point from every trackseg (this
improves cleaning as these points are often spurious).

Takes one argument, the path to the file to process
Options:
--suffix <string>: change the file suffix
--destination <string>: specify a destination folder for the processed file
--crop: turn on cropping of first and last trackpoints
--minpoints <integer>: set the maximum number of points a track must have
See --help for details

I call it preprocesssing because I have several processes to go
through before the file is accepted into our spatialite reference
database. So this is a preliminary step before running
[gpx2spatialite] (https://github.com/ptrv/gpx2spatialite)