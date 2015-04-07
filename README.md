# Geospatial Demo App

This is an example implementation of a location-based service to demonstrate the power of Cassandra, node.js and Websockets.
It provides three basic services/pages: 
* Check-in from the user's actual position (determined via the HTML5 Geolocation API)
* Show the current checkin-ins live
* Check-in to a location nearby the user's position

## Technologies

* [node.js](http://nodejs.org): General Platform
* [Cassandra](http://cassandra.apache.org): NoSQL database
* [Express](http://expressjs.com): Middleware Framework
* [Socket.io](http://socket.io): Messaging library
* [Leaflet](http://leafletjs.com): JavaScript mapping library
* [HTML5 Geolocation API](http://www.w3schools.com/html/html5_geolocation.asp): Locate user's position

## Installation

You will need [node.js](http://nodejs.org) and Cassandra to run the demo server. 

You can install the demo server via:

	npm install

This will download not only the package's dependencies but also the UlmApi example data from [daten.ulmapi.de](http://daten.ulmapi.de/_utils/database.html?haltestellen) and imports it into a fresh MongoDB collection called `haltestellen` (german for bus stops) inside the `geospatial-demo` database. A geospatial index for the `geometry.features.geometry.coordinates` field is automatically created.

Simple start the server via:

	npm start

## Pages

* `/checkin-simple.html` - Check-in at user's position
* `/checkin.html` - Check-in at a bus stop in the city of Ulm, Germany
* `/show.html` - Show check-ins live
