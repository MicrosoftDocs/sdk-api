---
UID: NS:http._HTTP_RESPONSE_V1
title: HTTP_RESPONSE_V1 (http.h)
description: Contains data associated with an HTTP response.
helpviewer_keywords: ["*PHTTP_RESPONSE","*PHTTP_RESPONSE_V1","HTTP_RESPONSE","HTTP_RESPONSE_V1","HTTP_RESPONSE_V1 structure [HTTP]","PHTTP_RESPONSE_V1","PHTTP_RESPONSE_V1 structure pointer [HTTP]","http.http_response_v1","http/HTTP_RESPONSE_V1","http/PHTTP_RESPONSE_V1"]
old-location: http\http_response_v1.htm
tech.root: http
ms.assetid: 9e1bbcca-1b7c-4146-95c7-72660bf31507
ms.date: 12/05/2018
ms.keywords: '*PHTTP_RESPONSE, *PHTTP_RESPONSE_V1, HTTP_RESPONSE, HTTP_RESPONSE_V1, HTTP_RESPONSE_V1 structure [HTTP], PHTTP_RESPONSE_V1, PHTTP_RESPONSE_V1 structure pointer [HTTP], http.http_response_v1, http/HTTP_RESPONSE_V1, http/PHTTP_RESPONSE_V1'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_RESPONSE_V1, *PHTTP_RESPONSE_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_RESPONSE_V1
 - http/_HTTP_RESPONSE_V1
 - PHTTP_RESPONSE_V1
 - http/PHTTP_RESPONSE_V1
 - HTTP_RESPONSE_V1
 - http/HTTP_RESPONSE_V1
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
 - HTTP_RESPONSE_V1
---

# HTTP_RESPONSE_V1 structure


## -description

The 
<b>HTTP_RESPONSE_V1</b> structure contains data associated with an HTTP response.

Do not use <b>HTTP_RESPONSE_V1</b> directly in your code;  use <a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.

## -struct-fields

### -field Flags

The optional logging flags change the default response behavior.     These  can be one of any of the  <a href="/windows/desktop/Http/http-response-flag--constants">HTTP_RESPONSE_FLAG</a> values.

### -field Version

This member is ignored; the response is always an HTTP/1.1 response.

### -field StatusCode

Numeric status code that characterizes the result of the HTTP request (for example, 200 signifying "OK" or 404 signifying "Not Found"). For more information and a list of these codes, see Section 10 of 
<a href="https://www.ietf.org/rfc/rfc2616.txt">RFC 2616</a>.

If a request is directed to a URL that is reserved but not registered, indicating that the appropriate application to handle it is not running, then the HTTP Server API itself returns a response with status code 400, signifying "Bad Request". This is transparent to the application. A code 400 is preferred here to 503 ("Server not available") because the latter is interpreted by some smart load balancers as an indication that the server is overloaded.

### -field ReasonLength

Size, in bytes, of the string pointed to by the <b>pReason</b> member not including the terminating null. May be zero.

### -field pReason

A pointer to a human-readable, null-terminated string of printable characters that characterizes the result of the HTTP request (for example, "OK" or "Not Found").

### -field Headers

An 
<a href="/windows/desktop/api/http/ns-http-http_response_headers">HTTP_RESPONSE_HEADERS</a> structure that contains the headers used in this response.

### -field EntityChunkCount

A number of entity-body data blocks specified in the <b>pEntityChunks</b> array. This number cannot exceed 100. If the response has no entity body, this member must be zero.

### -field pEntityChunks

An array of 
<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a> structures that together specify all the data blocks that make up the entity body of the response.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_response_headers">HTTP_RESPONSE_HEADERS</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v2">HTTP_RESPONSE_V2</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>