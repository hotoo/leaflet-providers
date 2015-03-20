
# Example

----

<link type="text/css" rel="stylesheet" href="../spm_modules/leaflet/0.7.3/leaflet.css" />

<div id="map-demo" style="height:300px"></div>


````js
seajs.use(['jquery', 'leaflet', 'leaflet-providers'], function($, L){

  // map
  var map = L.map('map-demo', {
      center: new L.LatLng(37, 120),
      zoom: 4,
      // zoomControl: false,
      fullscreenControl: true,
      layers: [
        L.tileLayer(
          'http://mt{s}.google.cn/vt/lyrs=m&hl=zh-CN&gl=cn&x={x}&y={y}&z={z}', {
            attribution: 'Google',
            subdomains: [0,1,2,3]
          }),
        L.tileLayer.provider('Esri.WorldStreetMap')
      ]
  });

})
````
