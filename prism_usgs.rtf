{\rtf1\ansi\ansicpg1252\cocoartf2761
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 // selects images within a specific date range.\
var start_date = '1995-01-01'\
var end_date = '2024-12-31'\
\
// Define an array of USGS IDs\
var usgsES = [  "12305000","12322000","13092747","13150430","13154500","13176400","13190500","13192200","13211205","13213000","13296000","13304050","13307000","13310800","13310850","13311000","13311250","13311450","13317660","13337095","13340000","13340600","13341050","13342500"\
];\
var latS = [  48.6168833,48.99638889,42.5625,43.3233611,43.0022222,42.26136944,43.3436111,43.55055556,43.67735278,43.78166667,44.27888889,44.68879167,45.3225,44.90225,44.88952778,44.9057222,44.93477778,44.9363611,46.00305556,46.0470361,46.4783333,46.84055556,46.50027778,46.4483333  \
];\
var lonS = [ \
  -116.0491944,-116.5075,-114.4947222,-114.10835,-115.2025,-116.8684417,-115.4775,-115.7219444,-116.7011306,-116.9727778,-114.7338889,-113.3704056,-114.44,-115.3256667,-115.3602222,-115.3295,-115.3366944,-115.3372222,-116.9169444,-115.866161,-116.2575,-115.621111,-116.3925,-116.8275\
  ];\
\
var samplePoint = function(image) \{\
  // Get the image date\
  var date = image.date().format('YYYY-MM-dd');\
  \
  // Sample the image at the point\
  var value = image.reduceRegion(\{\
    reducer: ee.Reducer.first(),\
    geometry: point,\
    scale: 10,\
  \});\
\
  // Return a feature with the date and sampled value\
  return ee.Feature(null, value).set('date', date);\
\};\
\
// Loop through the array\
for (var i = 0; i < usgsES.length; i++) \{\
  print('USGS ID:', usgsES[i]);\
  print("lat:", latS[i]);\
  print("lon:", lonS[i]);\
  \
  var file_name = usgsES[i] //+ "lat"+ latS[i]\
  \
  var tmean = ee.ImageCollection('OREGONSTATE/PRISM/AN81d')\
                  .filter(ee.Filter.date( start_date ,  end_date ))\
                  .select('tmean');\
                  \
  var properties = tmean.get('description');\
//  print('Description:', properties);\
\
  // Define a point of interest using latitude and longitude\
  var point = ee.Geometry.Point([ lonS[i], latS[i]  ]);\
  // Map the function over the collection\
  var sampledValues = tmean.map(samplePoint);\
\
// Print the results\
  print('Sampled Values:', sampledValues);\
\
// Convert to a FeatureCollection for export\
  var sampledFeatureCollection = ee.FeatureCollection(sampledValues);\
\
// Export the result to Google Drive\
  Export.table.toDrive(\{\
    collection: sampledFeatureCollection,\
    description:  file_name ,\
    fileFormat: 'CSV'\
  \});\
  \
\}}