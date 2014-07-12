leaflet-map
===========

*leaflet-map* is a web-component which provides access to the [leaflet map](http://leafletjs.com) 
JavaScript library via html elements.

Please have a look at the [demo page](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html) or the [api documentation](https://nhnb.github.io/leaflet-map/doc.html#leaflet-map).

Most of the options documented in the Leaflet reference are exported as html attributes. 
All events are mapped into html events of the same name.</p>
For example use &lt;leaflet-map latitude="51.505" longitude="-0.09" zoom="13"&gt; &lt;/leaflet-map&gt; 
to define the view and zoom level.


Web-components are an emerging standard which is based on Custom Elements, Shadow DOM, HTML Imports and Web Animations.
[Polymer](http://www.polymer-project.org/docs/start/tutorial/intro.html) is a library which simplifies working with web-components. It includes a compatibility layer for browsers which
do not yet support web-components natively, yet.


Status
======

Although leaflet-map is still under heavy development, it is already fully usable.

Lists of demos: 

* [leaflet-map](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#view) (L.map)
* [leaflet-marker](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#marker) (L.marker)
* [leaflet-icon](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#icon) (L.icon)
* [leaflet-divicon](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#icon) (L.divicon) (since 0.0.1)
* [leaflet-scale-control](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#scale) (L.control.scale) (since 0.2.0)
* [leaflet-tilelayer](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#tilelayer) (L.tileLayer)
* [leaflet-tilelayer-wms](https://nhnb.github.io/leaflet-map/leaflet-map/demo.html#layerwms) (L.tileLayer.wms)  (since 0.0.2)
* [leaflet-geolocation](https://nhnb.github.io/leaflet-map/leaflet-map/demo-advanced.html#databinding) (part of L.map) (since 0.0.2)


Dependencies
============

leaflet-map depends on Polymer in ../platform and ../polymer and it expects an installation of leaflet in ../leaflet.

Please note that the pages have to be accessed via a webserver. file://-urls are not supported.


Notes for implementing child elements
=====================================

Child elements like markers or layers will be initialized by the surrounding map by setting a "map" javascript property.
Therefore the child element should define a mapChanged method and use that as initializer. 
Don't forget to define a detached method to support removal of elements. The leaflet-marker element is a good template.  


License
=======

* [Leaflet](https://github.com/Leaflet/Leaflet/blob/master/LICENSE)
* [Polymer](https://github.com/polymer/polymer/blob/master/LICENSE)


Copyright (c) 2014, Hendrik Brummermann
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are
permitted provided that the following conditions are met:

   1. Redistributions of source code must retain the above copyright notice, this list of
      conditions and the following disclaimer.

   2. Redistributions in binary form must reproduce the above copyright notice, this list
      of conditions and the following disclaimer in the documentation and/or other materials
      provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY
EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR
TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

