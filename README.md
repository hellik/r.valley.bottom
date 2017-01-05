# r.valley.bottom
r.valley.bottom calculates a Multi-resolution Valley Bottom Flatness (MrVBF) index.

NAME
r.valley.bottom - Calculation of Multi-resolution Valley Bottom Flatness (MrVBF) index

KEYWORDS
raster, terrain

SYNOPSIS
r.valley.bottom
r.valley.bottom --help
r.valley.bottom [-s] elevation=name [--help] [--verbose] [--quiet] [--ui]
Flags:

-s
    Use square moving window instead of moving window in 8 directions
--help
    Print usage summary
--verbose
    Verbose module output
--quiet
    Quiet module output
--ui
    Force launching GUI dialog

Parameters:

elevation=name [required]
    Name of elevation raster map

DESCRIPTION
r.valley.bottom calculates a Multi-resolution Valley Bottom Flatness (MrVBF) index. The user must specify the input elevation raster map.

Default moving window is cells in 8 directions. With the -s flag a square moving window is used in calculations.

EXAMPLE

  # align region to DEM and habitat vector
  g.region -a raster=DEM align=DEM

  # run r.valley.bottom
  r.r.valley.bottom elevation=DEM

NOTES
experimental

TODO
Design the script independent of input elevation raster resolution. At the moment the input elevation raster map must have a resolution of 25m x 25m. Additionally the search window of the elevation percentile may be adapted.

SEE ALSO
r.mapcalc, r.slope.aspect

REFERENCES
J.C. Gallant & T.I. Dowling 2003. A multiresolution index of valley bottom flatness for mapping depositional areas. Water Resources Research, Vol. 39, No. 12, 1347. doi:10.1029/2002WR001426

AUTHOR
Helmut Kudrnovsky
