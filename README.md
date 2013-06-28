mapbox-animated-timeline
========================
So in summary we have something basic working. It can be enhanced more, much more

Here are the basics.

1. Technologies

 I used javascript libraries (mapbox.js and Leaflet.js) together with css and html.
 http://leafletjs.com/reference.html
 http://www.mapbox.com/mapbox.js/api/v1.1.0/

2. The data.

 The data is expected in the format shown in example-keyword-data.js. Namely, an array of dictionaries that have properties: year, month,location,keyword,strength

3. The workflow.

3.1 Preprocessing the data (done once per data)

First the data needs to be converted to a format called GeoJSON (http://www.geojson.org/) that mapbox.js works with. For the purpose, you need to open the file convertToGseoJSON.html. This file loads the data from example-keyword-data.js and for each location sends a query to get the coordinates of the place. Now, the html shows a lot of dialog windows but this was a fast way to syc the asynchronous calls that are made. I am sure there is a better way.
 Important: Once the dialogs are over, you need to copy the content of the page into example-gseojson-data.js

3.2 Visualization

Now you can start mapchart-anim.html. You'll see a map. On the top right you have 4 button. the first 3 show the situation for a specific month. The 4th (Play) shown an animation.
