---
UID: NS:http._HTTP_RESPONSE_HEADERS
title: HTTP_RESPONSE_HEADERS (http.h)
description: Contains the headers sent with an HTTP response.
helpviewer_keywords: ["*PHTTP_RESPONSE_HEADERS","HTTP_RESPONSE_HEADERS","HTTP_RESPONSE_HEADERS structure [HTTP]","PHTTP_RESPONSE_HEADERS","PHTTP_RESPONSE_HEADERS structure pointer [HTTP]","_http_http_response_headers","http.http_response_headers","http/HTTP_RESPONSE_HEADERS","http/PHTTP_RESPONSE_HEADERS"]
old-location: http\http_response_headers.htm
tech.root: http
ms.assetid: e783c27e-d215-4f6d-a080-92d915a7fc33
ms.date: 12/05/2018
ms.keywords: '*PHTTP_RESPONSE_HEADERS, HTTP_RESPONSE_HEADERS, HTTP_RESPONSE_HEADERS structure [HTTP], PHTTP_RESPONSE_HEADERS, PHTTP_RESPONSE_HEADERS structure pointer [HTTP], _http_http_response_headers, http.http_response_headers, http/HTTP_RESPONSE_HEADERS, http/PHTTP_RESPONSE_HEADERS'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HTTP_RESPONSE_HEADERS, *PHTTP_RESPONSE_HEADERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_RESPONSE_HEADERS
 - http/_HTTP_RESPONSE_HEADERS
 - PHTTP_RESPONSE_HEADERS
 - http/PHTTP_RESPONSE_HEADERS
 - HTTP_RESPONSE_HEADERS
 - http/HTTP_RESPONSE_HEADERS
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
 - HTTP_RESPONSE_HEADERS
---

# HTTP_RESPONSE_HEADERS structure


## -description

The 
<b>HTTP_RESPONSE_HEADERS</b> structure contains the headers sent with an HTTP response.

## -struct-fields

### -field UnknownHeaderCount

A number of unknown headers sent with the HTTP response and contained in the array pointed to by the <b>pUnknownHeaders</b> member. This number cannot exceed 9999.

### -field pUnknownHeaders

A pointer to an array of 
<a href="/windows/desktop/api/http/ns-http-http_unknown_header">HTTP_UNKNOWN_HEADER</a> structures that contains one structure for each of the unknown headers sent in the HTTP response.

### -field TrailerCount

This member is reserved and must be zero.

### -field pTrailers

This member is reserved and must be <b>NULL</b>.

### -field KnownHeaders

Fixed-size array of 
<a href="/windows/desktop/api/http/ns-http-http_known_header">HTTP_KNOWN_HEADER</a> structures. The 
<a href="/windows/desktop/api/http/ne-http-http_header_id">HTTP_HEADER_ID</a> enumeration provides a mapping from header types to array indexes. If a known header of a given type is included in the HTTP response, the array element at the index that corresponds to that type specifies the header value. Those elements of the array for which no corresponding headers are present contain a zero-valued <b>RawValueLength</b> member. Use <b>RawValueLength</b> to determine the end of the header string pointed to by <b>pRawValue</b>, rather than relying on the string to have a terminating null.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_known_header">HTTP_KNOWN_HEADER</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_unknown_header">HTTP_UNKNOWN_HEADER</a>