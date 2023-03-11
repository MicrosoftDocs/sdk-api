---
UID: NE:http._HTTP_REQUEST_PROPERTY
title: HTTP_REQUEST_PROPERTY (http.h)
description: Defines the properties that are configured by the HTTP Server API on a request.
helpviewer_keywords: ["*PHTTP_REQUEST_PROPERTY","*PHTTP_REQUEST_PROPERTY enumeration [HTTP]","HTTP_REQUEST_PROPERTY","HTTP_REQUEST_PROPERTY enumeration [HTTP]","HttpRequestPropertyStreamError","http.http_Request_property","http/*PHTTP_REQUEST_PROPERTY","http/HTTP_REQUEST_PROPERTY","http/HttpRequestPropertyStreamError"]
old-location: http\http_Request_property.htm
tech.root: http
ms.assetid: 02e40197-4e21-4268-8a5e-f9b222f7eba2
ms.date: 03/22/2021
ms.keywords: '*PHTTP_REQUEST_PROPERTY, *PHTTP_REQUEST_PROPERTY enumeration [HTTP], HTTP_REQUEST_PROPERTY, HTTP_REQUEST_PROPERTY enumeration [HTTP], HttpRequestPropertyStreamError, http.http_Request_property, http/*PHTTP_REQUEST_PROPERTY, http/HTTP_REQUEST_PROPERTY, http/HttpRequestPropertyStreamError'
req.header: http.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: HTTP_REQUEST_PROPERTY, *PHTTP_REQUEST_PROPERTY
req.redist:
ms.custom:
f1_keywords:
 - _HTTP_REQUEST_PROPERTY
 - http/_HTTP_REQUEST_PROPERTY
 - PHTTP_REQUEST_PROPERTY
 - http/PHTTP_REQUEST_PROPERTY
 - HTTP_REQUEST_PROPERTY
 - http/HTTP_REQUEST_PROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_REQUEST_PROPERTY
---

# HTTP_REQUEST_PROPERTY enumeration


## -description

The **HTTP\_REQUEST\_PROPERTY** enumeration defines the properties that are configured by the HTTP Server API on a request.

## -enum-fields

### -field HttpRequestPropertyStreamError

The HTTP/2 or HTTP/3 stream error on the request.

The [HTTP\_REQUEST\_PROPERTY\_STREAM\_ERROR](/windows/win32/api/http/ns-http-http_request_property_stream_error) structure contains the configuration data for this property.

## -remarks

The **HTTP\_REQUEST\_PROPERTY** enumeration types are used to set or query the configurations on a request. A member of this enumeration together with the associated configuration structure is used by [HttpSetRequestProperty](/windows/desktop/api/http/nf-http-httpsetrequestproperty) to define the configuration parameters.

## -see-also

[HttpSetRequestProperty](/windows/desktop/api/http/nf-http-httpsetrequestproperty)
