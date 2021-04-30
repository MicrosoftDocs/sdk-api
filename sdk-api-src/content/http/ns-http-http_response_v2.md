---
UID: NS:http._HTTP_RESPONSE_V2
title: HTTP_RESPONSE_V2 (http.h)
description: Extends the HTTP version 1.0 response structure with more information for the response.
helpviewer_keywords: ["*PHTTP_RESPONSE","*PHTTP_RESPONSE_V2","*PHTTP_RESPONSE_V2 structure [HTTP]","HTTP_RESPONSE","HTTP_RESPONSE_V2","HTTP_RESPONSE_V2 structure [HTTP]","http.http_response_v2","http/*PHTTP_RESPONSE_V2","http/HTTP_RESPONSE_V2"]
old-location: http\http_response_v2.htm
tech.root: http
ms.assetid: 1900741e-f466-4826-b376-36170176c30a
ms.date: 12/05/2018
ms.keywords: '*PHTTP_RESPONSE, *PHTTP_RESPONSE_V2, *PHTTP_RESPONSE_V2 structure [HTTP], HTTP_RESPONSE, HTTP_RESPONSE_V2, HTTP_RESPONSE_V2 structure [HTTP], http.http_response_v2, http/*PHTTP_RESPONSE_V2, http/HTTP_RESPONSE_V2'
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
req.typenames: HTTP_RESPONSE_V2, *PHTTP_RESPONSE_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_RESPONSE_V2
 - http/_HTTP_RESPONSE_V2
 - PHTTP_RESPONSE_V2
 - http/PHTTP_RESPONSE_V2
 - HTTP_RESPONSE_V2
 - http/HTTP_RESPONSE_V2
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
 - HTTP_RESPONSE_V2
---

# HTTP_RESPONSE_V2 structure


## -description

The <b>HTTP_RESPONSE_V2</b> structure extends the HTTP version 1.0 response structure with more information for the response.

Do not use <b>HTTP_RESPONSE_V2</b> directly in your code;  use <a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.

## -struct-fields

### -field ResponseInfoCount

The number of <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structures in the array pointed to by <b>pResponseInfo</b>.

The count of the HTTP_RESPONSE_INFO elements in the array pointed to by <b>pResponseInfo</b>.

### -field pResponseInfo

A pointer to an array of <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structures containing more information about the request.

### -field _HTTP_RESPONSE_V1

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_response_headers">HTTP_RESPONSE_HEADERS</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v1">HTTP_RESPONSE_V1</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>