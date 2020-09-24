---
UID: NS:http._HTTP_KNOWN_HEADER
title: HTTP_KNOWN_HEADER (http.h)
description: Contains the header values for a known header from an HTTP request or HTTP response.
helpviewer_keywords: ["*PHTTP_KNOWN_HEADER","HTTP_KNOWN_HEADER","HTTP_KNOWN_HEADER structure [HTTP]","PHTTP_KNOWN_HEADER","PHTTP_KNOWN_HEADER structure pointer [HTTP]","_http_http_known_header","http.http_known_header","http/HTTP_KNOWN_HEADER","http/PHTTP_KNOWN_HEADER"]
old-location: http\http_known_header.htm
tech.root: http
ms.assetid: 3f6c295c-f2c1-4070-a79e-9bb1e684ef92
ms.date: 12/05/2018
ms.keywords: '*PHTTP_KNOWN_HEADER, HTTP_KNOWN_HEADER, HTTP_KNOWN_HEADER structure [HTTP], PHTTP_KNOWN_HEADER, PHTTP_KNOWN_HEADER structure pointer [HTTP], _http_http_known_header, http.http_known_header, http/HTTP_KNOWN_HEADER, http/PHTTP_KNOWN_HEADER'
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
req.typenames: HTTP_KNOWN_HEADER, *PHTTP_KNOWN_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_KNOWN_HEADER
 - http/_HTTP_KNOWN_HEADER
 - PHTTP_KNOWN_HEADER
 - http/PHTTP_KNOWN_HEADER
 - HTTP_KNOWN_HEADER
 - http/HTTP_KNOWN_HEADER
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
 - HTTP_KNOWN_HEADER
---

# HTTP_KNOWN_HEADER structure


## -description

The 
<b>HTTP_KNOWN_HEADER</b> structure contains the header values for a known header from an HTTP request or HTTP response.

## -struct-fields

### -field RawValueLength

Size, in bytes,  of the 8-bit string pointed to by the <b>pRawValue</b> member, not counting a terminating null character, if present. If <b>RawValueLength</b> is zero, then the value of the <b>pRawValue</b> element is meaningless.

### -field pRawValue

Pointer to the text of this HTTP header. Use <b>RawValueLength</b> to determine where this text ends rather than relying on the string to have a terminating null. The format of the header text is specified in 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

## -remarks

In the HTTP Server API, known headers are defined as those that are enumerated in the 
<a href="/windows/desktop/api/http/ne-http-http_header_id">HTTP_HEADER_ID</a> enumeration type. Be aware that there are different lists of different sizes for request and response headers.

For more information about the structure and usage of HTTP headers, see the 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/windows/desktop/api/http/ne-http-http_header_id">HTTP_HEADER_ID</a>



<a href="/windows/desktop/api/http/ns-http-http_request_headers">HTTP_REQUEST_HEADERS</a>



<a href="/windows/desktop/api/http/ns-http-http_response_headers">HTTP_RESPONSE_HEADERS</a>