# L.basemapControl

A Leaflet plugin that provides a customizable basemap control for switching between different map layers. This plugin adds a new control to your Leaflet map, allowing users to switch between predefined basemaps with a simple click.

## Features

- Easily switch between multiple basemap layers.
- Preview the next basemap layer before applying it.
- Customizable layer options and control position.


## Demo

Check out a live demo of the plugin in action: [example/example1.html](https://urban96.github.io/L.basemapControl/example/example1.html)


## Example usage

To use the `L.basemapControl` plugin, follow these steps:

1. **Include the plugin's CSS and JavaScript files** in your HTML file:

    ```html
    <link rel="stylesheet" href="path/to/L.basemapControl.min.css">
    <script src="path/to/L.basemapControl.min.js"></script>
    ```

2. **Initialize the control** on your map with the desired layers:

    ```javascript
    // Initialize the Leaflet map
    var map = L.map('map').setView([51.505, -0.09], 13);


    // Initialize the basemap control
    var basemapControl = L.basemapControl({
        position: 'bottomleft',
        layers: [
            {
                layer: L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
                    maxZoom: 19,
                    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
                })
            },
            {
                layer: L.tileLayer('https://tileserver.memomaps.de/tilegen/{z}/{x}/{y}.png', {
                    maxZoom: 18,
                    attribution: 'Map <a href="https://memomaps.de/">memomaps.de</a> <a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, map data &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
                })
            },
            {
                layer: L.tileLayer('https://{s}.tile.opentopomap.org/{z}/{x}/{y}.png', {
                    maxZoom: 17,
                    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
                })
            }
        ]
    }).addTo(map);
    ```

3. **Customize** the `position` and `layers` options as needed for your application.

Make sure you have initialized your Leaflet map and included the plugin’s CSS and JS files before using the `L.basemapControl`.
