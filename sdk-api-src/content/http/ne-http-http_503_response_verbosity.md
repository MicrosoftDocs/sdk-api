---
UID: NE:http._HTTP_503_RESPONSE_VERBOSITY
title: HTTP_503_RESPONSE_VERBOSITY (http.h)
description: The HTTP_503_RESPONSE_VERBOSITY enumeration defines the verbosity levels for a 503, service unavailable, error responses.This structure must be used when setting or querying the HttpServer503ResponseProperty on a request queue.
helpviewer_keywords: ["*PHTTP_503_RESPONSE_VERBOSITY","*PHTTP_503_RESPONSE_VERBOSITY enumeration [HTTP]","HTTP_503_RESPONSE_VERBOSITY","HTTP_503_RESPONSE_VERBOSITY enumeration [HTTP]","Http503ResponseVerbosityBasic","Http503ResponseVerbosityFull","Http503ResponseVerbosityLimited","http.http_503_response_verbosity","http/*PHTTP_503_RESPONSE_VERBOSITY","http/HTTP_503_RESPONSE_VERBOSITY","http/Http503ResponseVerbosityBasic","http/Http503ResponseVerbosityFull","http/Http503ResponseVerbosityLimited"]
old-location: http\http_503_response_verbosity.htm
tech.root: http
ms.assetid: e103bdf4-dc48-45ba-84dc-4161310ee3ff
ms.date: 12/05/2018
ms.keywords: '*PHTTP_503_RESPONSE_VERBOSITY, *PHTTP_503_RESPONSE_VERBOSITY enumeration [HTTP], HTTP_503_RESPONSE_VERBOSITY, HTTP_503_RESPONSE_VERBOSITY enumeration [HTTP], Http503ResponseVerbosityBasic, Http503ResponseVerbosityFull, Http503ResponseVerbosityLimited, http.http_503_response_verbosity, http/*PHTTP_503_RESPONSE_VERBOSITY, http/HTTP_503_RESPONSE_VERBOSITY, http/Http503ResponseVerbosityBasic, http/Http503ResponseVerbosityFull, http/Http503ResponseVerbosityLimited'
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
req.typenames: HTTP_503_RESPONSE_VERBOSITY, *PHTTP_503_RESPONSE_VERBOSITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_503_RESPONSE_VERBOSITY
 - http/_HTTP_503_RESPONSE_VERBOSITY
 - PHTTP_503_RESPONSE_VERBOSITY
 - http/PHTTP_503_RESPONSE_VERBOSITY
 - HTTP_503_RESPONSE_VERBOSITY
 - http/HTTP_503_RESPONSE_VERBOSITY
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
 - HTTP_503_RESPONSE_VERBOSITY
---

# HTTP_503_RESPONSE_VERBOSITY enumeration


## -description

The <b>HTTP_503_RESPONSE_VERBOSITY</b> enumeration defines the verbosity levels for a 503, service unavailable, error responses.

This structure must be used when setting or querying the <a href="/windows/desktop/api/http/ne-http-http_server_property">HttpServer503ResponseProperty</a> on a request queue.

## -enum-fields

### -field Http503ResponseVerbosityBasic

A 503 response is not sent; the connection is reset.
    This is the default HTTP Server API behavior.

### -field Http503ResponseVerbosityLimited

The HTTP Server API sends a 503 response with a "Service Unavailable" reason phrase. The HTTP Server closes the TCP connection after sending the response, so the client has to re-connect.

### -field Http503ResponseVerbosityFull

The HTTP Server API sends a 503 response with a detailed reason phrase. The HTTP Server closes the TCP connection after sending the response, so the client has to re-connect.

## -remarks

This enumeration is used in <a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>, and <a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryrequestQueueProperty</a> to set and query the 503  response verbosity. The <i>pPropertyInformation</i> parameter points to a member of the <b>HTTP_503_RESPONSE_VERBOSITY</b> enumeration when the <i>Property</i> parameter is <b>HttpServer503VerbosityProperty</b>.

This enumeration defines the verbosity level for a request queue when sending 503 (Service Unavailable) error responses. Note that the 503 response level set using the <b>HTTP_503_RESPONSE_VERBOSITY</b>  enumeration only affects the error responses generated internally
 by the HTTP Server API.


<div class="alert"><b>Note</b>  Disclosing information about the state of the service to potentially unsafe clients may pose a security risk.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>