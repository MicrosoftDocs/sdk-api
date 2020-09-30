---
UID: NS:http._HTTP_UNKNOWN_HEADER
title: HTTP_UNKNOWN_HEADER (http.h)
description: Contains the name and value for a header in an HTTP request or response whose name does not appear in the enumeration.
helpviewer_keywords: ["*PHTTP_UNKNOWN_HEADER","HTTP_UNKNOWN_HEADER","HTTP_UNKNOWN_HEADER structure [HTTP]","PHTTP_UNKNOWN_HEADER","PHTTP_UNKNOWN_HEADER structure pointer [HTTP]","_http_http_unknown_header","http.http_unknown_header","http/HTTP_UNKNOWN_HEADER","http/PHTTP_UNKNOWN_HEADER"]
old-location: http\http_unknown_header.htm
tech.root: http
ms.assetid: 158f2979-58d3-4120-a74a-311b6fc53136
ms.date: 12/05/2018
ms.keywords: '*PHTTP_UNKNOWN_HEADER, HTTP_UNKNOWN_HEADER, HTTP_UNKNOWN_HEADER structure [HTTP], PHTTP_UNKNOWN_HEADER, PHTTP_UNKNOWN_HEADER structure pointer [HTTP], _http_http_unknown_header, http.http_unknown_header, http/HTTP_UNKNOWN_HEADER, http/PHTTP_UNKNOWN_HEADER'
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
req.typenames: HTTP_UNKNOWN_HEADER, *PHTTP_UNKNOWN_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_UNKNOWN_HEADER
 - http/_HTTP_UNKNOWN_HEADER
 - PHTTP_UNKNOWN_HEADER
 - http/PHTTP_UNKNOWN_HEADER
 - HTTP_UNKNOWN_HEADER
 - http/HTTP_UNKNOWN_HEADER
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
 - HTTP_UNKNOWN_HEADER
---

# HTTP_UNKNOWN_HEADER structure


## -description

The 
<b>HTTP_UNKNOWN_HEADER</b> structure contains the name and value for a header in an HTTP request or response whose name does not appear in the enumeration.

## -struct-fields

### -field NameLength

The size, in bytes, of the data pointed to by the <b>pName</b> member not counting a terminating null.

### -field RawValueLength

The size, in bytes, of the data pointed to by the <b>pRawValue</b> member, in bytes.

### -field pName

A pointer to a string of octets that specifies the header name. Use <b>NameLength</b> to determine the end of the string, rather than relying on a terminating <b>null</b>.

### -field pRawValue

A pointer to a string of octets that specifies the values for this header. Use <b>RawValueLength</b> to determine the end of the string, rather than relying on a terminating <b>null</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_header_id">HTTP_HEADER_ID</a>



<a href="/windows/desktop/api/http/ns-http-http_request_headers">HTTP_REQUEST_HEADERS</a>



<a href="/windows/desktop/api/http/ns-http-http_response_headers">HTTP_RESPONSE_HEADERS</a>