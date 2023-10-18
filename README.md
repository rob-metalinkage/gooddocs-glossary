# gooddocs-glossary
Demonstration of download and semantic uplift of GoodDocs terminology glossary.

This repository automates conversion of a Google Sheet form into a standardised semantic model using JSON-LD - easily consumed by either JSON or RDF environments.

The source is configured in [.config/config.yml](.config/config.yml).

The output is in [downloaded.csv.ttl](downloaded.csv.ttl)

The workflow can be triggered manually from 
https://github.com/rob-metalinkage/gooddocs-glossary/actions/workflows/download-and-uplift.yaml


# Demo from spreadsheet
## Files

- `.config/`: OGC tools configuration
  - `config.yml`: General configuration (download URLs and target files) 
  - `catalog.ttl`: Domain Configuration catalog with uplift definition for `*.csv.json` files.
  - `csv2python.yml`: Uplift definition that simply turns CSV into JSON
  - `properties-uplift.yml`: Uplift definition that takes the JSONified CSV and converts it to JSON-LD and Turtle
- `.github/workflows/`: GitHub workflows
  - `download-and-uplift.yaml`: Downloads the spreadsheet and performs the conversion and uplift steps

## See also

- [OGC Naming Authority tools (ogc-na)](https://opengeospatial.github.io/ogc-na-tools/)
  - [Domain configuration and uplift context examples](https://opengeospatial.github.io/ogc-na-tools/examples/)
  - [ingest_json reference](https://opengeospatial.github.io/ogc-na-tools/reference/ogc/na/ingest_json/)
  - [CSV input filter configuration](https://opengeospatial.github.io/ogc-na-tools/reference/ogc/na/input_filters/csv/)
