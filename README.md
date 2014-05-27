GMaps_styles.js - Add style to your GMaps.js Javascript library.
=========================================================

GMaps.js allows you to use the potential of Google Maps in a simple way. No more extensive documentation or large amount of code.

Visit the examples in [hpneo.github.com/gmaps](http://hpneo.github.com/gmaps/)
Go to the API Documentation [hpneo.github.io/gmaps/documentation.html](http://hpneo.github.io/gmaps/documentation.html)

How to use
------

```html
<script type='text/javascript' src='//maps.google.com/maps/api/js?sensor=true'></script>
<script type='text/javascript' src='gmaps_styles.js'></script>
<script type='text/javascript' src='gmaps.js'></script>
```

```html
<div id="map"></div>
<script type="text/javascript">
 (function($) { "use strict";
	var map;
	$(document).ready(function(){
	
		// Default GMaps.js setup
		map = new GMaps({
			div         : '#map',
			lat         : 45.745204,
			lng         : -73.622578,
			zoom        : 11,
			mapTypeControlOptions: {
				mapTypeIds: [google.maps.MapTypeId.ROADMAP, 'map_style']
			}
		});
		
		// Add 'simple-atlas' style to your Map
		var map_styles = new GMaps_styles();
		var data_styles = map_styles.datas('simple-atlas');
		map.addStyle({
		  styles 			: data_styles.styles,
		  styledMapName		: data_styles.mapName,
		  mapTypeId 		: 'map_style'
		});
		map.setStyle( 'map_style' );
	
	});
 })(jQuery);
</script>
```

Current style accepted

```html
light-political
dark-landmass
light-landmass
mono-city
simple-atlas
whitewater
```


Changelog
---------

0.1.1 - Initial release
-----------------------
* Initial examples and project



License
---------
MIT License. Copyright 2014 Alfred Dagenais. https://github.com/KilukruMedia

Permission is hereby granted, free of charge, to any
person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the
Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice
shall be included in all copies or substantial portions of
the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY
KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.