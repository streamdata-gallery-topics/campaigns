---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Update a batch
  description: Updates a single Batch instance, currently batch can only be turned
    "on/off"
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /campaigns/batches/{id}:
    get:
      summary: Find a specific batch
      description: Returns a single Batch instance for a given batch id. This API
        is useful for determining the state of a validating batch
      operationId: getCampaignBatch
      x-api-path-slug: campaignsbatchesid-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a batch
      responses:
        200:
          description: OK
      tags:
      - Campaigns
      - Batches
    put:
      summary: Update a batch
      description: Updates a single Batch instance, currently batch can only be turned
        "on/off"
      operationId: updateCampaignBatch
      x-api-path-slug: campaignsbatchesid-put
      parameters:
      - in: body
        name: body
        description: A batch instance
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: An id of a batch to update
      responses:
        200:
          description: OK
      tags:
      - Campaigns
      - Batches
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