---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 0
info:
  title: Data.gov API Get Spatial Zones S
  description: Fetch a zone list as GeoJSON
  version: "3"
host: catalog.data.gov
basePath: /api/3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /spatial/coverage/{level}:
    get:
      summary: Get Spatial Coverage Level
      description: List each zone for a given level with their datasets count
      operationId: getSpatialCoverageLevel
      x-api-path-slug: spatialcoveragelevel-get
      parameters:
      - in: path
        name: level
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Coverage
      - Level
  /spatial/granularities:
    get:
      summary: Get Spatial Granularities
      description: List all known spatial granularities
      operationId: getSpatialGranularities
      x-api-path-slug: spatialgranularities-get
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Granularities
  /spatial/levels:
    get:
      summary: Get Spatial Levels
      description: List all known levels
      operationId: getSpatialLevels
      x-api-path-slug: spatiallevels-get
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Levels
  /spatial/zone/{id}:
    get:
      summary: Get Spatial Zone
      description: Fetch a zone
      operationId: getSpatialZone
      x-api-path-slug: spatialzoneid-get
      parameters:
      - in: path
        name: id
        description: A zone identifier
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Zone
  /spatial/zones/suggest:
    get:
      summary: Get Spatial Zones Suggest
      description: Suggest geospatial zones
      operationId: getSpatialZonesSuggest
      x-api-path-slug: spatialzonessuggest-get
      parameters:
      - in: query
        name: q
        description: The string to autocomplete/suggest
      - in: query
        name: size
        description: The amount of suggestion to fetch
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Zones
      - Suggest
  /spatial/zones/{ids}:
    get:
      summary: Get Spatial Zones S
      description: Fetch a zone list as GeoJSON
      operationId: getSpatialZonesS
      x-api-path-slug: spatialzonesids-get
      parameters:
      - in: path
        name: ids
        description: A zone identifiers list (comma separated)
      responses:
        200:
          description: OK
      tags:
      - Spatial
      - Zones
      - S
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---