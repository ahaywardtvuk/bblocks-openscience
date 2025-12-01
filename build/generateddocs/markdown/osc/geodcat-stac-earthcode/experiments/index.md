
# EarthCODE Experiment (Schema)

`ogc.osc.geodcat-stac-earthcode.experiments` *v0.1*

EarthCODE metadata profile linked to semantic models

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## ESA EarthCODE experiments as GeoDCAT and STAC profile 

This building block shows a possible profile of GeoDCAT supporting semantic annotation and inclusion of the three STAC extensions used by EarthCODE:

- themes
- osc
- cf

## Examples

### An example demonstrating a basic EarthCODE Experiment
#### json
```json
{
  "id": "polaris-experiment",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,
  "properties": {
    "created": "2025-02-19T23:00:00Z",
    "updated": "2025-02-19T23:00:00Z",
    "type": "experiment",
    "title": "POLARIS",
    "description": "Polar Operational Limit Assessment Risk Index System (POLARIS)",
    "keywords": [
      "sea ice",
      "polar"
    ],
    "contacts": [
      {
        "name": "EarthCODE Demo",
        "organization": "EarthCODE",
        "links": [
          {
            "rel": "about",
            "type": "text/html",
            "href": "https://opensciencedata.esa.int/"
          }
        ],
        "contactInstructions": "Contact via EarthCODE",
        "roles": [
          "host"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "oceans"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "CC-BY-SA-4.0",
    "osc:workflow": "polaris-workflow",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "../../catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "../catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "../../products/polaris/collection.json",
      "type": "application/json",
      "title": "POLARIS"
    },
    {
      "rel": "related",
      "href": "../../themes/oceans/catalog.json",
      "type": "application/json",
      "title": "Theme: Oceans"
    },
    {
      "rel": "related",
      "href": "../../workflows/polaris-workflow/record.json",
      "type": "application/json",
      "title": "Workflow: POLARIS"
    },
    {
      "rel": "input",
      "href": "./input.yaml",
      "type": "application/yaml",
      "title": "Input parameters"
    },
    {
      "rel": "environment",
      "href": "./environment.yaml",
      "type": "application/yaml",
      "title": "Execution environment"
    },
    {
      "rel": "self",
      "href": "https://esa-earthcode.github.io/open-science-catalog-metadata/experiments/polaris-experiment/item.json",
      "type": "application/json"
    }
  ]
}

```

#### jsonld
```jsonld
{
  "@context": "https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/context.jsonld",
  "id": "polaris-experiment",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,
  "properties": {
    "created": "2025-02-19T23:00:00Z",
    "updated": "2025-02-19T23:00:00Z",
    "type": "experiment",
    "title": "POLARIS",
    "description": "Polar Operational Limit Assessment Risk Index System (POLARIS)",
    "keywords": [
      "sea ice",
      "polar"
    ],
    "contacts": [
      {
        "name": "EarthCODE Demo",
        "organization": "EarthCODE",
        "links": [
          {
            "rel": "about",
            "type": "text/html",
            "href": "https://opensciencedata.esa.int/"
          }
        ],
        "contactInstructions": "Contact via EarthCODE",
        "roles": [
          "host"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "oceans"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "CC-BY-SA-4.0",
    "osc:workflow": "polaris-workflow",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "../../catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "../catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "../../products/polaris/collection.json",
      "type": "application/json",
      "title": "POLARIS"
    },
    {
      "rel": "related",
      "href": "../../themes/oceans/catalog.json",
      "type": "application/json",
      "title": "Theme: Oceans"
    },
    {
      "rel": "related",
      "href": "../../workflows/polaris-workflow/record.json",
      "type": "application/json",
      "title": "Workflow: POLARIS"
    },
    {
      "rel": "input",
      "href": "./input.yaml",
      "type": "application/yaml",
      "title": "Input parameters"
    },
    {
      "rel": "environment",
      "href": "./environment.yaml",
      "type": "application/yaml",
      "title": "Execution environment"
    },
    {
      "rel": "self",
      "href": "https://esa-earthcode.github.io/open-science-catalog-metadata/experiments/polaris-experiment/item.json",
      "type": "application/json"
    }
  ]
}
```

#### ttl
```ttl
@prefix : <https://w3id.org/ogc/stac/assets/> .
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix ns2: <osc:> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix stac: <https://w3id.org/ogc/stac/core/> .
@prefix thns: <https://w3id.org/ogc/stac/themes/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://ogc.org/demo/ospd/polaris-experiment> a geojson:Feature ;
    dcterms:conformsTo <http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core> ;
    rdfs:seeAlso [ rdfs:label "Open Science Catalog" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/root> ;
            oa:hasTarget <https://ogc.org/catalog.json> ],
        [ rdfs:label "POLARIS" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/child> ;
            oa:hasTarget <https://ogc.org/products/polaris/collection.json> ],
        [ rdfs:label "Execution environment" ;
            dcterms:format "application/yaml" ;
            ns1:relation <http://www.iana.org/assignments/relation/environment> ;
            oa:hasTarget <https://ogc.org/demo/ospd/environment.yaml> ],
        [ rdfs:label "Input parameters" ;
            dcterms:format "application/yaml" ;
            ns1:relation <http://www.iana.org/assignments/relation/input> ;
            oa:hasTarget <https://ogc.org/demo/ospd/input.yaml> ],
        [ rdfs:label "Theme: Oceans" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://ogc.org/themes/oceans/catalog.json> ],
        [ dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/self> ;
            oa:hasTarget <https://esa-earthcode.github.io/open-science-catalog-metadata/experiments/polaris-experiment/item.json> ],
        [ rdfs:label "Experiments" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/parent> ;
            oa:hasTarget <https://ogc.org/demo/catalog.json> ],
        [ rdfs:label "Workflow: POLARIS" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://ogc.org/workflows/polaris-workflow/record.json> ] ;
    :properties [ a :experiment ;
            dcterms:created "2025-02-19T23:00:00Z" ;
            dcterms:description "Polar Operational Limit Assessment Risk Index System (POLARIS)" ;
            dcterms:modified "2025-02-19T23:00:00Z" ;
            dcterms:title "POLARIS" ;
            dcat:contactPoint [ :contactInstructions "Contact via EarthCODE" ;
                    :links [ dcterms:type "text/html" ;
                            ns1:relation <http://www.iana.org/assignments/relation/about> ;
                            oa:hasTarget <https://opensciencedata.esa.int/> ] ;
                    :name "EarthCODE Demo" ;
                    :organization "EarthCODE" ;
                    stac:roles "host" ] ;
            dcat:keyword "polar",
                "sea ice" ;
            dcat:license "CC-BY-SA-4.0" ;
            :version "2" ;
            rec:format [ rec:name "GeoTIFF" ] ;
            rec:themes [ thns:concepts [ thns:id "oceans"^^xsd:string ] ;
                    thns:scheme "https://github.com/stac-extensions/osc#theme" ] ;
            ns2:workflow "polaris-workflow" ] .


```


### An example Experiment for the OSPD experiment taking the water bodies workflow and running it on another platform.
#### json
```json
{
  "id": "water-bodies-execution",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,
  "properties": {
    "created": "2025-01-21T18:00:00Z",
    "updated": "2025-01-21T18:40:00Z",
    "type": "experiment",
    "title": "ESA WorldCereal Experiment",
    "description": "Experiment using the water bodies workflow.",
    "contacts": [
      {
        "name": "A person",
        "position": "Researcher",
        "organization": "An Org",
        "contactInstructions": "Contact via website",
        "roles": [
          "principal investigator"
        ]
      },
      {
        "name": "An Org",
        "links": [
          {
            "href": "https://example.com/",
            "rel": "about",
            "type": "text/html"
          }
        ],
        "contactInstructions": "SEE WEBSITE",
        "roles": [
          "processor"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "land"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "proprietary",
    "osc:workflow": "waterbodies",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "https://example.com/open-science-catalog-metadata/catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "https://example.com/open-science-catalog-metadata/experiments/catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json",
      "type": "application/json",
      "title": "Water Bodies Execution Outputs"
    },
    {
      "rel": "service",
      "type": "application/json",
      "title": "An EO data exploitation platform",
      "href": "https://example.com"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/themes/land/catalog.json",
      "type": "application/json",
      "title": "Theme: Land"
    },
    {
      "rel": "related",
      "href": "../../workflows/waterbodies/record.json",
      "type": "application/json",
      "title": "Workflow: Water Bodies"
    },
    {
      "rel": "self",
      "href": "https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json",
      "type": "application/json"
    }
  ]
}

```

#### jsonld
```jsonld
{
  "@context": "https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/context.jsonld",
  "id": "water-bodies-execution",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,
  "properties": {
    "created": "2025-01-21T18:00:00Z",
    "updated": "2025-01-21T18:40:00Z",
    "type": "experiment",
    "title": "ESA WorldCereal Experiment",
    "description": "Experiment using the water bodies workflow.",
    "contacts": [
      {
        "name": "A person",
        "position": "Researcher",
        "organization": "An Org",
        "contactInstructions": "Contact via website",
        "roles": [
          "principal investigator"
        ]
      },
      {
        "name": "An Org",
        "links": [
          {
            "href": "https://example.com/",
            "rel": "about",
            "type": "text/html"
          }
        ],
        "contactInstructions": "SEE WEBSITE",
        "roles": [
          "processor"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "land"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "proprietary",
    "osc:workflow": "waterbodies",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "https://example.com/open-science-catalog-metadata/catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "https://example.com/open-science-catalog-metadata/experiments/catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json",
      "type": "application/json",
      "title": "Water Bodies Execution Outputs"
    },
    {
      "rel": "service",
      "type": "application/json",
      "title": "An EO data exploitation platform",
      "href": "https://example.com"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/themes/land/catalog.json",
      "type": "application/json",
      "title": "Theme: Land"
    },
    {
      "rel": "related",
      "href": "../../workflows/waterbodies/record.json",
      "type": "application/json",
      "title": "Workflow: Water Bodies"
    },
    {
      "rel": "self",
      "href": "https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json",
      "type": "application/json"
    }
  ]
}
```

#### ttl
```ttl
@prefix : <https://w3id.org/ogc/stac/assets/> .
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix ns2: <osc:> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix stac: <https://w3id.org/ogc/stac/core/> .
@prefix thns: <https://w3id.org/ogc/stac/themes/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://ogc.org/demo/ospd/water-bodies-execution> a geojson:Feature ;
    dcterms:conformsTo <http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core> ;
    rdfs:seeAlso [ rdfs:label "Water Bodies Execution Outputs" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/child> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json> ],
        [ dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/self> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json> ],
        [ rdfs:label "Open Science Catalog" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/root> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/catalog.json> ],
        [ rdfs:label "Theme: Land" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/themes/land/catalog.json> ],
        [ rdfs:label "Workflow: Water Bodies" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://ogc.org/workflows/waterbodies/record.json> ],
        [ rdfs:label "An EO data exploitation platform" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/service> ;
            oa:hasTarget <https://example.com> ],
        [ rdfs:label "Experiments" ;
            dcterms:format "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/parent> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/experiments/catalog.json> ] ;
    :properties [ a :experiment ;
            dcterms:created "2025-01-21T18:00:00Z" ;
            dcterms:description "Experiment using the water bodies workflow." ;
            dcterms:modified "2025-01-21T18:40:00Z" ;
            dcterms:title "ESA WorldCereal Experiment" ;
            dcat:contactPoint [ :contactInstructions "SEE WEBSITE" ;
                    :links [ dcterms:type "text/html" ;
                            ns1:relation <http://www.iana.org/assignments/relation/about> ;
                            oa:hasTarget <https://example.com/> ] ;
                    :name "An Org" ;
                    stac:roles "processor" ],
                [ :contactInstructions "Contact via website" ;
                    :name "A person" ;
                    :organization "An Org" ;
                    :position "Researcher" ;
                    stac:roles "principal investigator" ] ;
            dcat:license "proprietary" ;
            :version "2" ;
            rec:format [ rec:name "GeoTIFF" ] ;
            rec:themes [ thns:concepts [ thns:id "land"^^xsd:string ] ;
                    thns:scheme "https://github.com/stac-extensions/osc#theme" ] ;
            ns2:workflow "waterbodies" ] .


```


### The water bodies experiment with some provenance data attached
#### json
```json
{
  "id": "water-bodies-execution",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,

  "properties": {
    "prov": {
      "_comment": "This mocks up provenance information for the water bodies execution, first with plain prov then with wf4ever.",


      "id": "water-bodies-execution",
      "provType": [
        "Activity",
        "wfprov:WorkflowRun"
      ],
      "startedAtTime": "2025-01-21T17:40:50Z",
      "endedAtTime": "2025-01-21T17:59:50Z",
      "wasAssociatedWith": [
        {
          "agentType": "Person",
          "name": "A Person",
          "actedOnBehalfOf": {
            "agentType": "Organization",
            "name": "An Org"
          }
        }
      ],

      "qualifiedUsage": [
        {
          "type": "Usage",
          "entity": {
            "id": "ogc-api-inputs",
            "type": ["Entity", "wfprov:Artifact"],
            "data": {
              "stac_items": [
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
              ],
              "aoi": "-121.399,39.834,-120.74,40.472",
              "epsg": "EPSG:4326",
              "bands": [
                "green",
                "nir"
              ]
            }
          },
          "role": "Processes API inputs"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "aoi",
            "type": ["Entity", "wfprov:Artifact"],
            "data": "-121.399,39.834,-120.74,40.472"
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/aoi"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "stac_items",
            "type": ["Entity", "wfprov:Artifact"],
            "hadMember": [
              "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
              "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
            ]
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/stac_items"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "epsg",
            "type": ["Entity", "wfprov:Artifact"],
            "data": "EPSG:4326"
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/epsg"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "bands",
            "type": ["Entity", "prov:Collection", "wfprov:Artifact"],
            "hadMember": [
              {
                "value": "green"
              },
              {
                "value": "nir"
              }
            ]
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/bands"
        }
      ],

      "generated": [
        "https://example.com/products/water-bodies/collection.json"
      ],


      
      "wfprov:describedByWorkflow": "https://example.com/workflows/waterbodies/record.json",
      "wfprov:wasEnactedBy": { 
        "id": "eo-data-platform",
        "type": ["wfprov:WorkfowEngine", "prov:SoftwareAgent", "prov:Agent"],
        "prov:label": "cwltool 3.1.20251031082601"
      },
      "wfprov:usedInput": [
        {
          "type": "wfprov:Artifact",
          "hadMember": [
            "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
            "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
          ],
          "describedByParameter": "stac_items"
        },
        {
          "type": "wfprov:Artifact",
          "data": "-121.399,39.834,-120.74,40.472",
          "describedByParameter": "aoi"
        },
        {
          "type": "wfprov:Artifact",
          "data": "EPSG:4326",
          "describedByParameter": "epsg"
        },
        {
          "type": "wfprov:Artifact",
          "data": [
              "green",
              "nir"
          ],
          "describedByParameter": "bands"
        }
      ]
    },


    "created": "2025-01-21T18:00:00Z",
    "updated": "2025-01-21T18:40:00Z",
    "type": "experiment",
    "title": "Water Bodies Experiment",
    "description": "Experiment using the water bodies workflow.",
    "contacts": [
      {
        "name": "A person",
        "position": "Researcher",
        "organization": "An Org",
        "contactInstructions": "Contact via website",
        "roles": [
          "principal investigator"
        ]
      },
      {
        "name": "An Org",
        "links": [
          {
            "href": "https://example.com/",
            "rel": "about",
            "type": "text/html"
          }
        ],
        "contactInstructions": "SEE WEBSITE",
        "roles": [
          "processor"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "land"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "proprietary",
    "osc:workflow": "waterbodies",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "https://example.com/open-science-catalog-metadata/catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "https://example.com/open-science-catalog-metadata/experiments/catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json",
      "type": "application/json",
      "title": "Water Bodies Execution Outputs"
    },
    {
      "rel": "service",
      "type": "application/json",
      "title": "An EO data exploitation platform",
      "href": "https://example.com"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/themes/land/catalog.json",
      "type": "application/json",
      "title": "Theme: Land"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/workflows/waterbodies/record.json",
      "type": "application/json",
      "title": "Workflow: Water Bodies"
    },
    {
      "rel": "self",
      "href": "https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json",
      "type": "application/json"
    }
  ]
}

```

#### jsonld
```jsonld
{
  "@context": "https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/context.jsonld",
  "id": "water-bodies-execution",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "geometry": null,
  "properties": {
    "prov": {
      "_comment": "This mocks up provenance information for the water bodies execution, first with plain prov then with wf4ever.",
      "id": "water-bodies-execution",
      "provType": [
        "Activity",
        "wfprov:WorkflowRun"
      ],
      "startedAtTime": "2025-01-21T17:40:50Z",
      "endedAtTime": "2025-01-21T17:59:50Z",
      "wasAssociatedWith": [
        {
          "agentType": "Person",
          "name": "A Person",
          "actedOnBehalfOf": {
            "agentType": "Organization",
            "name": "An Org"
          }
        }
      ],
      "qualifiedUsage": [
        {
          "type": "Usage",
          "entity": {
            "id": "ogc-api-inputs",
            "type": [
              "Entity",
              "wfprov:Artifact"
            ],
            "data": {
              "stac_items": [
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
              ],
              "aoi": "-121.399,39.834,-120.74,40.472",
              "epsg": "EPSG:4326",
              "bands": [
                "green",
                "nir"
              ]
            }
          },
          "role": "Processes API inputs"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "aoi",
            "type": [
              "Entity",
              "wfprov:Artifact"
            ],
            "data": "-121.399,39.834,-120.74,40.472"
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/aoi"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "stac_items",
            "type": [
              "Entity",
              "wfprov:Artifact"
            ],
            "hadMember": [
              "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
              "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
            ]
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/stac_items"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "epsg",
            "type": [
              "Entity",
              "wfprov:Artifact"
            ],
            "data": "EPSG:4326"
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/epsg"
        },
        {
          "type": "Usage",
          "entity": {
            "id": "bands",
            "type": [
              "Entity",
              "prov:Collection",
              "wfprov:Artifact"
            ],
            "hadMember": [
              {
                "value": "green"
              },
              {
                "value": "nir"
              }
            ]
          },
          "role": "https://example.com/workflows/water-bodies/record.json#main/bands"
        }
      ],
      "generated": [
        "https://example.com/products/water-bodies/collection.json"
      ],
      "wfprov:describedByWorkflow": "https://example.com/workflows/waterbodies/record.json",
      "wfprov:wasEnactedBy": {
        "id": "eo-data-platform",
        "type": [
          "wfprov:WorkfowEngine",
          "prov:SoftwareAgent",
          "prov:Agent"
        ],
        "prov:label": "cwltool 3.1.20251031082601"
      },
      "wfprov:usedInput": [
        {
          "type": "wfprov:Artifact",
          "hadMember": [
            "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A",
            "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A"
          ],
          "describedByParameter": "stac_items"
        },
        {
          "type": "wfprov:Artifact",
          "data": "-121.399,39.834,-120.74,40.472",
          "describedByParameter": "aoi"
        },
        {
          "type": "wfprov:Artifact",
          "data": "EPSG:4326",
          "describedByParameter": "epsg"
        },
        {
          "type": "wfprov:Artifact",
          "data": [
            "green",
            "nir"
          ],
          "describedByParameter": "bands"
        }
      ]
    },
    "created": "2025-01-21T18:00:00Z",
    "updated": "2025-01-21T18:40:00Z",
    "type": "experiment",
    "title": "Water Bodies Experiment",
    "description": "Experiment using the water bodies workflow.",
    "contacts": [
      {
        "name": "A person",
        "position": "Researcher",
        "organization": "An Org",
        "contactInstructions": "Contact via website",
        "roles": [
          "principal investigator"
        ]
      },
      {
        "name": "An Org",
        "links": [
          {
            "href": "https://example.com/",
            "rel": "about",
            "type": "text/html"
          }
        ],
        "contactInstructions": "SEE WEBSITE",
        "roles": [
          "processor"
        ]
      }
    ],
    "themes": [
      {
        "scheme": "https://github.com/stac-extensions/osc#theme",
        "concepts": [
          {
            "id": "land"
          }
        ]
      }
    ],
    "formats": [
      {
        "name": "GeoTIFF"
      }
    ],
    "license": "proprietary",
    "osc:workflow": "waterbodies",
    "version": "2"
  },
  "linkTemplates": [],
  "links": [
    {
      "rel": "root",
      "href": "https://example.com/open-science-catalog-metadata/catalog.json",
      "type": "application/json",
      "title": "Open Science Catalog"
    },
    {
      "rel": "parent",
      "href": "https://example.com/open-science-catalog-metadata/experiments/catalog.json",
      "type": "application/json",
      "title": "Experiments"
    },
    {
      "rel": "child",
      "href": "https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json",
      "type": "application/json",
      "title": "Water Bodies Execution Outputs"
    },
    {
      "rel": "service",
      "type": "application/json",
      "title": "An EO data exploitation platform",
      "href": "https://example.com"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/themes/land/catalog.json",
      "type": "application/json",
      "title": "Theme: Land"
    },
    {
      "rel": "related",
      "href": "https://example.com/open-science-catalog-metadata/workflows/waterbodies/record.json",
      "type": "application/json",
      "title": "Workflow: Water Bodies"
    },
    {
      "rel": "self",
      "href": "https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json",
      "type": "application/json"
    }
  ]
}
```

#### ttl
```ttl
@prefix : <https://w3id.org/ogc/stac/assets/> .
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <wfprov:> .
@prefix ns2: <http://www.iana.org/assignments/> .
@prefix ns3: <osc:> .
@prefix ns4: <prov:> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix stac: <https://w3id.org/ogc/stac/core/> .
@prefix thns: <https://w3id.org/ogc/stac/themes/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://ogc.org/demo/ospd/aoi> a :Entity,
        ns1:Artifact ;
    :data "-121.399,39.834,-120.74,40.472" .

<https://ogc.org/demo/ospd/bands> a :Entity,
        ns4:Collection,
        ns1:Artifact ;
    :hadMember [ :value "nir" ],
        [ :value "green" ] .

<https://ogc.org/demo/ospd/eo-data-platform> a ns4:Agent,
        ns4:SoftwareAgent,
        ns1:WorkfowEngine ;
    ns4:label "cwltool 3.1.20251031082601" .

<https://ogc.org/demo/ospd/epsg> a :Entity,
        ns1:Artifact ;
    :data "EPSG:4326" .

<https://ogc.org/demo/ospd/ogc-api-inputs> a :Entity,
        ns1:Artifact ;
    :data [ :aoi "-121.399,39.834,-120.74,40.472" ;
            :bands "green",
                "nir" ;
            :epsg "EPSG:4326" ;
            :stac_items "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A",
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A" ] .

<https://ogc.org/demo/ospd/stac_items> a :Entity,
        ns1:Artifact ;
    :hadMember "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A",
        "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A" .

<https://ogc.org/demo/ospd/water-bodies-execution> a geojson:Feature ;
    dcterms:conformsTo <http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core> ;
    rdfs:seeAlso [ rdfs:label "Theme: Land" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/themes/land/catalog.json> ],
        [ rdfs:label "Workflow: Water Bodies" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/workflows/waterbodies/record.json> ],
        [ dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/self> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/experiments/water-bodies-execution/record.json> ],
        [ rdfs:label "Water Bodies Execution Outputs" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/child> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/products/water-bodies-execution-outputs/collection.json> ],
        [ rdfs:label "Experiments" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/parent> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/experiments/catalog.json> ],
        [ rdfs:label "An EO data exploitation platform" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/service> ;
            oa:hasTarget <https://example.com> ],
        [ rdfs:label "Open Science Catalog" ;
            dcterms:format "application/json" ;
            ns2:relation <http://www.iana.org/assignments/relation/root> ;
            oa:hasTarget <https://example.com/open-science-catalog-metadata/catalog.json> ] ;
    :_comment "This mocks up provenance information for the water bodies execution, first with plain prov then with wf4ever." ;
    :endedAtTime "2025-01-21T17:59:50Z" ;
    :generated "https://example.com/products/water-bodies/collection.json" ;
    :properties [ a :experiment ;
            dcterms:created "2025-01-21T18:00:00Z" ;
            dcterms:description "Experiment using the water bodies workflow." ;
            dcterms:modified "2025-01-21T18:40:00Z" ;
            dcterms:title "Water Bodies Experiment" ;
            dcat:contactPoint [ :contactInstructions "SEE WEBSITE" ;
                    :links [ dcterms:type "text/html" ;
                            ns2:relation <http://www.iana.org/assignments/relation/about> ;
                            oa:hasTarget <https://example.com/> ] ;
                    :name "An Org" ;
                    stac:roles "processor" ],
                [ :contactInstructions "Contact via website" ;
                    :name "A person" ;
                    :organization "An Org" ;
                    :position "Researcher" ;
                    stac:roles "principal investigator" ] ;
            dcat:license "proprietary" ;
            :prov <https://ogc.org/demo/ospd/water-bodies-execution> ;
            :version "2" ;
            rec:format [ rec:name "GeoTIFF" ] ;
            rec:themes [ thns:concepts [ thns:id "land"^^xsd:string ] ;
                    thns:scheme "https://github.com/stac-extensions/osc#theme" ] ;
            ns3:workflow "waterbodies" ] ;
    :provType "Activity",
        "wfprov:WorkflowRun" ;
    :qualifiedUsage [ a :Usage ;
            :entity <https://ogc.org/demo/ospd/ogc-api-inputs> ;
            :role "Processes API inputs" ],
        [ a :Usage ;
            :entity <https://ogc.org/demo/ospd/stac_items> ;
            :role "https://example.com/workflows/water-bodies/record.json#main/stac_items" ],
        [ a :Usage ;
            :entity <https://ogc.org/demo/ospd/bands> ;
            :role "https://example.com/workflows/water-bodies/record.json#main/bands" ],
        [ a :Usage ;
            :entity <https://ogc.org/demo/ospd/aoi> ;
            :role "https://example.com/workflows/water-bodies/record.json#main/aoi" ],
        [ a :Usage ;
            :entity <https://ogc.org/demo/ospd/epsg> ;
            :role "https://example.com/workflows/water-bodies/record.json#main/epsg" ] ;
    :startedAtTime "2025-01-21T17:40:50Z" ;
    :wasAssociatedWith [ :actedOnBehalfOf [ :agentType "Organization" ;
                    :name "An Org" ] ;
            :agentType "Person" ;
            :name "A Person" ] ;
    ns1:describedByWorkflow "https://example.com/workflows/waterbodies/record.json" ;
    ns1:usedInput [ a ns1:Artifact ;
            :describedByParameter "stac_items" ;
            :hadMember "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2A_10TFK_20220524_0_L2A",
                "https://earth-search.aws.element84.com/v0/collections/sentinel-s2-l2a-cogs/items/S2B_10TFK_20210713_0_L2A" ],
        [ a ns1:Artifact ;
            :data "green",
                "nir" ;
            :describedByParameter "bands" ],
        [ a ns1:Artifact ;
            :data "EPSG:4326" ;
            :describedByParameter "epsg" ],
        [ a ns1:Artifact ;
            :data "-121.399,39.834,-120.74,40.472" ;
            :describedByParameter "aoi" ] ;
    ns1:wasEnactedBy <https://ogc.org/demo/ospd/eo-data-platform> .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: EarthCode Experiment
allOf:
- $ref: https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/common/schema.yaml
- $ref: https://ogcincubator.github.io/geodcat-ogcapi-records/build/annotated/geo/geodcat/geodcat-records/schema.yaml
properties:
  properties:
    type: object
    required:
    - osc:workflow
    properties:
      osc:workflow:
        $ref: https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/common/schema.yaml#/$defs/osc:workflow
      prov:
        $ref: https://ogcincubator.github.io/bblock-prov-schema/build/annotated/ogc-utils/prov-activity/schema.yaml
  links:
    type: array
    items:
      oneOf:
      - title: Other Link
        properties:
          rel:
            not:
              enum:
              - via
              - input
              - environment
      - title: Link to Input Parameter
        properties:
          rel:
            const: input
      - title: Link to Execution Environment
        properties:
          rel:
            const: environment
      - $ref: https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/common/schema.yaml#/$defs/via_links

```

Links to the schema:

* YAML version: [schema.yaml](https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/schema.json)
* JSON version: [schema.json](https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "type": "@type",
    "id": "@id",
    "properties": {},
    "geometry": {
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        },
        "geometries": {}
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "links": {
      "@context": {
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:format",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent",
        "anchor": {},
        "method": {},
        "headers": {},
        "body": {}
      },
      "@id": "rdfs:seeAlso"
    },
    "conformsTo": {
      "@container": "@set",
      "@id": "dct:conformsTo",
      "@type": "@id"
    },
    "time": {
      "@context": {
        "date": {},
        "timestamp": {},
        "interval": {},
        "resolution": {}
      },
      "@id": "dct:temporal"
    },
    "linkTemplates": {
      "@context": {
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:format",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent",
        "uriTemplate": {
          "@type": "xsd:string",
          "@id": "rec:uriTemplate"
        },
        "varBase": "rec:varBase",
        "variables": {
          "@id": "rec:hasVariable",
          "@container": "@index",
          "@index": "dct:identifier"
        }
      },
      "@id": "rec:hasLinkTemplate"
    },
    "created": "dct:created",
    "updated": "dct:modified",
    "title": {
      "@container": "@set",
      "@id": "dct:title"
    },
    "description": {
      "@container": "@set",
      "@id": "dct:description"
    },
    "keywords": {
      "@container": "@set",
      "@id": "dcat:keyword"
    },
    "language": {
      "@id": "rec:language",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel",
        "alternate": {},
        "dir": {}
      }
    },
    "languages": {
      "@container": "@set",
      "@id": "rec:languages",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel",
        "alternate": {},
        "dir": {}
      }
    },
    "resourceLanguages": {
      "@container": "@set",
      "@id": "rec:resourceLanguages",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel",
        "alternate": {},
        "dir": {}
      }
    },
    "externalIds": {
      "@container": "@set",
      "@id": "rec:scopedIdentifier",
      "@context": {
        "scheme": "rec:scheme",
        "value": "rec:id"
      }
    },
    "themes": {
      "@container": "@set",
      "@id": "rec:themes",
      "@context": {
        "concepts": {
          "@id": "thns:concepts",
          "@context": {
            "id": {
              "@type": "xsd:string",
              "@id": "thns:id"
            },
            "url": {
              "@type": "@id",
              "@id": "@id"
            }
          },
          "@container": "@set"
        }
      }
    },
    "formats": {
      "@id": "rec:format",
      "@context": {
        "name": "rec:name",
        "mediaType": "rec:mediaType"
      },
      "@container": "@set",
      "@type": "@id"
    },
    "contacts": {
      "@container": "@set",
      "@id": "dcat:contactPoint",
      "@type": "@id",
      "@context": {
        "identifier": {},
        "name": {},
        "position": {},
        "organization": {},
        "logo": {
          "@context": {
            "rel": {
              "@context": {
                "@base": "http://www.iana.org/assignments/relation/"
              },
              "@id": "http://www.iana.org/assignments/relation",
              "@type": "@id"
            },
            "anchor": {},
            "type": "dct:type",
            "hreflang": "dct:language",
            "title": "rdfs:label",
            "length": "dct:extent"
          }
        },
        "phones": {
          "@context": {
            "value": {}
          }
        },
        "emails": {
          "@context": {
            "value": {}
          }
        },
        "addresses": {
          "@context": {
            "deliveryPoint": {},
            "city": {},
            "administrativeArea": {},
            "postalCode": {},
            "country": {}
          }
        },
        "links": {
          "@context": {
            "rel": {
              "@context": {
                "@base": "http://www.iana.org/assignments/relation/"
              },
              "@id": "http://www.iana.org/assignments/relation",
              "@type": "@id"
            },
            "anchor": {},
            "type": "dct:type",
            "hreflang": "dct:language",
            "title": "rdfs:label",
            "length": "dct:extent"
          }
        },
        "hoursOfService": {},
        "contactInstructions": {}
      }
    },
    "license": "dcat:license",
    "accessrights": "dct:accessRights",
    "variables": {
      "@container": "@id",
      "@id": "rec:hasVariable",
      "@context": {
        "@base": "http://example.com/variables/",
        "@vocab": "https://www.opengis.net/def/ogc-api/records/"
      }
    },
    "collection": {},
    "stac_extensions": "stac:hasExtension",
    "roles": {
      "@id": "stac:roles",
      "@container": "@set"
    },
    "bands": {
      "@context": {
        "name": {}
      }
    },
    "datetime": {
      "@id": "dct:date",
      "@type": "xsd:dateTime"
    },
    "start_datetime": {},
    "end_datetime": {},
    "data_type": {},
    "nodata": {},
    "statistics": {
      "@context": {
        "minimum": {},
        "maximum": {},
        "mean": {},
        "stddev": {},
        "count": {},
        "valid_percent": {}
      }
    },
    "unit": {},
    "platform": {},
    "instruments": {},
    "constellation": {},
    "mission": {},
    "gsd": {},
    "providers": {
      "@context": {
        "name": {},
        "url": {}
      }
    },
    "rights": "dcat:rights",
    "@vocab": "https://w3id.org/ogc/stac/assets/",
    "assets": {
      "@context": {
        "type": "dct:format"
      },
      "@id": "stac:hasAsset",
      "@container": "@set"
    },
    "stac_version": "stac:version",
    "media_type": "dct:format",
    "extent": {
      "@id": "dct:extent",
      "@context": {
        "spatial": {},
        "temporal": {
          "@context": {
            "interval": {}
          }
        }
      }
    },
    "item_assets": {},
    "summaries": {
      "@context": {
        "minimum": {},
        "maximum": {}
      }
    },
    "concepts": {
      "@id": "thns:concepts",
      "@container": "@set",
      "@context": {
        "name": "thns:name",
        "id": "thns:id",
        "url": "@id"
      }
    },
    "scheme": "thns:scheme",
    "osc:type": {},
    "osc:status": {},
    "osc:project": {},
    "osc:region": {},
    "osc:variables": {},
    "osc:missions": {},
    "osc:experiment": {},
    "osc:workflows": {},
    "osc:workflow": {},
    "prov": {},
    "rel": {},
    "href": {
      "@type": "@id",
      "@id": "oa:hasTarget"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "dcat": "http://www.w3.org/ns/dcat#",
    "rec": "https://www.opengis.net/def/ogc-api/records/",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "w3ctime": "http://www.w3.org/2006/time#",
    "dctype": "http://purl.org/dc/dcmitype/",
    "vcard": "http://www.w3.org/2006/vcard/ns#",
    "foaf": "http://xmlns.com/foaf/0.1/",
    "thns": "https://w3id.org/ogc/stac/themes/",
    "stac": "https://w3id.org/ogc/stac/core/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ahaywardtvuk.github.io/bblocks-openscience/build/annotated/osc/geodcat-stac-earthcode/experiments/context.jsonld)

## Sources

* [GeoDCAT Specification](http://www.opengis.net/def/metamodel/profiles/geodcat)
* [EarthCODE]({
      "title": "GeoDCAT Specification",
      "link": "http://www.opengis.net/def/metamodel/profiles/geodcat"
    },)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ahaywardtvuk/bblocks-openscience](https://github.com/ahaywardtvuk/bblocks-openscience)
* Path: `_sources/geodcat-stac-earthcode/experiments`

