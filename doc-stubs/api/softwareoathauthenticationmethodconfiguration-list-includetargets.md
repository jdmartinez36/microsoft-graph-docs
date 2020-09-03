---
title: "List includeTargets"
description: "Get the authenticationMethodTargets from the includeTargets navigation property."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List includeTargets
Namespace: microsoft.graph

Get the authenticationMethodTargets from the includeTargets navigation property.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /qrAuthenticationMethodConfiguration/includeTargets
GET /smsAuthenticationMethodConfiguration/includeTargets
GET /fido2AuthenticationMethodConfiguration/includeTargets
GET /emailAuthenticationMethodConfiguration/includeTargets
GET /voiceAuthenticationMethodConfiguration/includeTargets
GET /passwordAuthenticationMethodConfiguration/includeTargets
GET /hardwareOathAuthenticationMethodConfiguration/includeTargets
GET /softwareOathAuthenticationMethodConfiguration/includeTargets
GET /temporaryAccessPassAuthenticationMethodConfiguration/includeTargets
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [authenticationMethodTarget](../resources/authenticationmethodtarget.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_authenticationmethodtarget"
}
-->
``` http
GET https://graph.microsoft.com/beta/qrAuthenticationMethodConfiguration/includeTargets
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.authenticationMethodTarget)"
}
-->
``` http
HTTP/1.1 200 OK

Content-Type: application/json
{
  "value": [
    {
      "@odata.type": "#microsoft.graph.authenticationMethodTarget",
      "id": "2a5e4d1f-4d1f-2a5e-1f4d-5e2a1f4d5e2a",
      "targetType": "String",
      "isRegistrationRequired": "Boolean",
      "useForSignIn": "Boolean"
    }
  ]
}
```
