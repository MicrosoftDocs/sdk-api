---
UID: NS:http._HTTP_REQUEST_V2
title: HTTP_REQUEST_V2 (http.h)
description: Extends the HTTP_REQUEST_V1 request structure with more information about the request.
helpviewer_keywords: ["*PHTTP_REQUEST","*PHTTP_REQUEST_V2","*PHTTP_REQUEST_V2 structure [HTTP]","HTTP_REQUEST","HTTP_REQUEST_V2","HTTP_REQUEST_V2 structure [HTTP]","http.http_request_v2","http/*PHTTP_REQUEST_V2","http/HTTP_REQUEST_V2"]
old-location: http\http_request_v2.htm
tech.root: http
ms.assetid: 02ac6f4f-ca54-42d5-9acb-5a1e81b2cb1c
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST, *PHTTP_REQUEST_V2, *PHTTP_REQUEST_V2 structure [HTTP], HTTP_REQUEST, HTTP_REQUEST_V2, HTTP_REQUEST_V2 structure [HTTP], http.http_request_v2, http/*PHTTP_REQUEST_V2, http/HTTP_REQUEST_V2'
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
req.typenames: HTTP_REQUEST_V2, *PHTTP_REQUEST_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_V2
 - http/_HTTP_REQUEST_V2
 - PHTTP_REQUEST_V2
 - http/PHTTP_REQUEST_V2
 - HTTP_REQUEST_V2
 - http/HTTP_REQUEST_V2
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
 - HTTP_REQUEST_V2
---

# HTTP_REQUEST_V2 structure


## -description

The <b>HTTP_REQUEST_V2</b> structure extends the <a href="/windows/desktop/api/http/ns-http-http_request_v1">HTTP_REQUEST_V1</a> request structure with more information about the request.

Do not use <b>HTTP_REQUEST_V2</b> directly in your code;  use <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.

## -struct-fields

### -field RequestInfoCount

The number of <a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a> structures in the array pointed to by <b>pRequestInfo</b>.

### -field pRequestInfo

A pointer to an array of <a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a> structures that contains additional information about the request.

### -field _HTTP_REQUEST_V1

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_cooked_url">HTTP_COOKED_URL</a>



<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/api/http/ns-http-http_request_v1">HTTP_REQUEST_V1</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_ssl_info">HTTP_SSL_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_transport_address">HTTP_TRANSPORT_ADDRESS</a>



<a href="/windows/desktop/api/http/ne-http-http_verb">HTTP_VERB</a>



<a href="/windows/desktop/api/http/nf-http-httpreceivehttprequest">HttpReceiveHttpRequest</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiverequestentitybody">HttpReceiveRequestEntityBody</a>



<a href="/windows/desktop/api/http/nf-http-httpsendhttpresponse">HttpSendHttpResponse</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>