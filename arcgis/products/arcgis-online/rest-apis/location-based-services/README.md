> **Note**: this page is only a draft, but this project is hosted on a [public repository](https://github.com/hhkaos/awesome-arcgis) where anyone can contribute. Learn how to [contribute in less than a minute](https://github.com/hhkaos/awesome-arcgis/blob/master/CONTRIBUTING.md#contributions).

# Location-based services

Location-based services, formerly known as `ready to use services` are several services hosted on [ArcGIS Online](../../README.md) that can be consumed though a REST API.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of contents**

- [Introduction](#introduction)
- [Services](#services)
  - [Geocoding (geocoder service)](#geocoding-geocoder-service)
  - [Routing and Directions (routing service)](#routing-and-directions-routing-service)
  - [Demographics and GeoEnrichment (GeoEnrichment service)](#demographics-and-geoenrichment-geoenrichment-service)
  - [Spatial Analysis (Spatial Analysis service)](#spatial-analysis-spatial-analysis-service)
  - [Elevation (Elevation service)](#elevation-elevation-service)
  - [Packaging (Offline Packaging Service)](#packaging-offline-packaging-service)
- [REST API to calculate credit consumption](#rest-api-to-calculate-credit-consumption)
- [More resources](#more-resources)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction

Some of theres are *free* and some consume [credits](../../credits/README.md), those that consume credits require to be [authenticated](../../../../name-users/oauth/README.md).

## Services

### Geocoding (geocoder service)

Service URL: [geocode.arcgis.com](https://geocode.arcgis.com)

Learn more about the [Geocoding and Place Search service](https://developers.arcgis.com/features/geocoding/) and the [Geocoder coverage](https://doc.arcgis.com/en/arcgis-online/reference/geocode-coverage.htm).

HowTos: [Geocoding API DevLabs](https://developers.arcgis.com/labs/browse/?topic=Geocoding&product=any)
[Overview of the World Geocoding Service](https://developers.arcgis.com/rest/geocode/api-reference/overview-world-geocoding-service.htm)

Trick: Custom geocoder with candidates filtered by URL: `http://geocode.arcgis.com/arcgis/rest/services/World/GeocodeServer?sourceCountry={{Country_code}}`

For example:
`http://geocode.arcgis.com/arcgis/rest/services/World/GeocodeServer?sourceCountry=ESP`


### Routing and Directions (routing service)

Service URLs: [route.arcgis.com](https://route.arcgis.com) & [logistics.arcgis.com](https://logistics.arcgis.com)

HowTos:
* [Routing API DevLabs](https://developers.arcgis.com/labs/browse/?topic=Routing&product=any)
* [Overview of network analysis services](https://developers.arcgis.com/rest/network/api-reference/overview-of-network-analysis-services.htm)
* [Routing on ArcGIS Online](http://odoe.net/blog/routing-arcgis-online/)

### Demographics and GeoEnrichment (GeoEnrichment service)

Service URL: [geoenrich.arcgis.com](https://geoenrich.arcgis.com)

HowTos:

* [GeoEnrichment API DevLabs](https://developers.arcgis.com/labs/browse/?topic=Demographics&product=any)
* [Uploading and enriching data to ArcCGIS Online](http://odoe.net/blog/uploading-enriching-data-arcgis-online/)
* [The GeoEnrichment service](https://developers.arcgis.com/rest/geoenrichment/api-reference/geoenrichment-service-overview.htm)

### Spatial Analysis (Spatial Analysis service)

Service URL: [analysis.arcgis.com](https://analysis.arcgis.com)

HowTos: [Spatial Analysis API DevLabs](https://developers.arcgis.com/labs/browse/?topic=Spatial-Analysis&product=any)
* [Overview of tasks contained in the Spatial Analysis service](https://developers.arcgis.com/rest/analysis/api-reference/tasks-overview.htm)

### Elevation (Elevation service)

Service URL: [elevation.arcgis.com](https://elevation.arcgis.com)

[Get started with Elevation Analysis services](https://developers.arcgis.com/rest/elevation/api-reference/get-started-with-elevation-services.htm)

### Packaging (Offline Packaging Service)

Service URL: [packaging.arcgis.com](https://packaging.arcgis.com)

[Get started](https://developers.arcgis.com/rest/packaging/api-reference/offline-packaging-service.htm)

## REST API to calculate credit consumption

This REST API is not documented but if you debug the **analysis tools** inside the [ArcGIS Online Web Viewer](http://www.arcgis.com/home/webmap/viewer.html) whenever you click the "Show credits" link you will find an AJAX request to this endpoint: `https://analysis.arcgis.com/arcgis/rest/services/tasks/GPServer/exts/Estimate/<OPERATION>`.

Use it to find the parameters you need to send in order to do the calculations.

## More resources

**Pending**:

* Geometry engine
* Print service
* ...
