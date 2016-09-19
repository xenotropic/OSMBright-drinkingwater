# OSMBright-drinkingwater
This contains some files to modify the osm-bright (a CartoCSS style for Open Street Maps) to display drinking water prominently. The original theme by MapBox is at https://github.com/mapbox/osm-bright

These edits:
* make freeways less prominent by a color change in the palette file
* fetches drinking water data based in a query added to osm-bright.osm2pgsql.mml 
* and displays amenity=drinking_water info starting at zoom level 10, which is in labels.mss. 
 
The osm-bright theme doesn't show amenity=drinking_water at all, since it is a more stripped-down style; the default OSM style shows it only at zoom level 16, which is quite close-in. This theme makes drinking water the most prominent feature of the map, to allow users to search for water sources easily and to allow for surveying large areas for completeness of coverage. 

I created this by following the directions to build a tile server at [switch2osm.org](https://switch2osm.org/serving-tiles/manually-building-a-tile-server-14-04/), and then hacking around with these files until I got drinking water displayed the way I wanted. The files all go in /usr/local/share/maps/style/osm-bright-master/osm-bright/, except the svg file goes in /usr/local/share/maps/style/osm-bright-master/osm-bright/img/icon/

You will need to recompile the style sheet after copying the files in -- see "Compiling the stylesheet" in the Switch2OSM tutorial.

![demo image of water map](https://raw.githubusercontent.com/xenotropic/OSMBright-drinkingwater/master/watermap-demo.jpg "Screenshot of the map using this edited style.")

