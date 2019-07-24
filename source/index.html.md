---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ

toc_footers:
  - TOC Footer

includes:
  - errors

search: true
---

# Introduction

This is the beginning of the EV Connect API reference document.  The intent of this document is that it will be checked into the code repository aso that we can track, version and review documentation.

# Tariffs

## Create a Tariff

### HTTP Request

`POST http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.

### Fields

Field | Required? | Description
----- | --------- | -----------
name | yes | The name of the plan.
description | no | The description of the plan.
tariffAltText |  no | Alternative text used to describe the tariff to the driver.
networkId | yes | The id of the network you want this to be under.
organizationId | yes | The id of the organization you want this to be under.
currency | no | The ISO 4217 currency code
tariffAltUrl | no | The alternative url pointing to a web resource describing the tariff.
elements | yes | List of EvCloud Tariff Elements.

<aside class="warning">
Yes, we know we have duplicated data required in the request and are addressing it as I type this...
</aside>

## Get a Specific Tariff

### HTTP Request

`GET http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs/{tariffId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
tariffId | yes | ExternalId og the tariff.

## Get All Tariffs for Organization

### HTTP Request

`GET http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.

## Update a Tariff

### HTTP Request

`PUT http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs/{tariffId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
tariffId | yes | External id of the tariff.

### Fields

Field | Description
----- | -----------
name | The name of the plan.
description | The description of the plan.
tariffAltText | Alternative text used to describe the tariff to the driver.
networkId | The id of the network you want this to be under.
organizationId | The id of the organization you want this to be under.
currency | The ISO 4217 currency code
tariffAltUrl | The alternative url pointing to a web resource describing the tariff.
elements | List of EvCloud Tariff Elements.

<aside class="warning">
Yes, we know we have duplicated data required in the request and are addressing it as I type this...
</aside>


## Delete a Specific Tariff

### HTTP Request

`DELETE http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs/{tariffId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
tariffId | yes | External id of the tariff.

## Get Tariff Alt Text

### HTTP Request

`GET http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/tariffs/altText/{language}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
tariffId | yes | External id of the tariff.

### Fields

Field | Description
----- | -----------
name | The name of the plan.
description | The description of the plan.
tariffAltText | Alternative text used to describe the tariff to the driver.
networkId | The id of the network you want this to be under.
organizationId | The id of the organization you want this to be under.
currency | The ISO 4217 currency code
tariffAltUrl | The alternative url pointing to a web resource describing the tariff.
elements | List of EvCloud Tariff Elements.

# Plans

## Create a Plan

### HTTP Request

`POST http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/plans`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.

### Fields

Field | Required? | Description
----- | --------- | -----------
networkId | yes | The id of the network you want this to be under.
organizationId | yes | The id of the organization you want this to be under.
name | yes | The name of the plan.
description | no | The description of the plan.
autoAccept | no | Use Auto Accept by matching email domain names.  True or False.
emailPatterns | no | List of regex patterns to match domain name against for Auto Accept feature.
guestPlan | no | Make this a guest plan <Enter description of guest plan here>.  True or False.
elements | yes | List of EvCloud Plan Elements.

<aside class="warning">
Yes, we know we have duplicated data required in the request and are addressing it as I type this...
</aside>

## Get a Specific {lan

### HTTP Request

`GET http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/plans/{planId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
planId | yes | External id of the plan.

## Get All Plans for Organization

### HTTP Request

`GET http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/plans`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.

## Update a Plan

### HTTP Request

`PUT http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/plans/{planId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
planId | yes | External id of the plan.

### Fields

Field | Description
----- | -----------
name | The name of the plan.
description | The description of the plan.

<aside class="warning">
Yes, we know we have duplicated data required in the request and are addressing it as I type this...
</aside>


## Delete a Specific Plan

### HTTP Request

`DELETE http://ops-demo.evconnect.com/api/rest/v5/networks/{networkId}/organizations/{organizationId}/plans/{planId}`

### URL Parameters

Parameter | Required | Description
--------- | ------- | -----------
networkId | yes | External id of network.
organizationId | yes | External id of organization.
planID | yes | External id of the plan.
