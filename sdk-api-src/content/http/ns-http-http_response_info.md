---
UID: NS:http._HTTP_RESPONSE_INFO
title: HTTP_RESPONSE_INFO (http.h)
description: Extends the HTTP_RESPONSE structure with additional information for the response.
helpviewer_keywords: ["*PHTTP_RESPONSE_INFO","*PHTTP_RESPONSE_INFO structure [HTTP]","HTTP_RESPONSE_INFO","HTTP_RESPONSE_INFO structure [HTTP]","http.http_response_info","http/*PHTTP_RESPONSE_INFO","http/HTTP_RESPONSE_INFO"]
old-location: http\http_response_info.htm
tech.root: http
ms.assetid: 29422116-0a33-4553-98aa-785bb926dee0
ms.date: 12/05/2018
ms.keywords: '*PHTTP_RESPONSE_INFO, *PHTTP_RESPONSE_INFO structure [HTTP], HTTP_RESPONSE_INFO, HTTP_RESPONSE_INFO structure [HTTP], http.http_response_info, http/*PHTTP_RESPONSE_INFO, http/HTTP_RESPONSE_INFO'
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
req.typenames: HTTP_RESPONSE_INFO, *PHTTP_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_RESPONSE_INFO
 - http/_HTTP_RESPONSE_INFO
 - PHTTP_RESPONSE_INFO
 - http/PHTTP_RESPONSE_INFO
 - HTTP_RESPONSE_INFO
 - http/HTTP_RESPONSE_INFO
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
 - HTTP_RESPONSE_INFO
---

# HTTP_RESPONSE_INFO structure


## -description

The <b>HTTP_RESPONSE_INFO</b> structure extends the <a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a> structure  with additional information for the response.

## -struct-fields

### -field Type

A member of the <a href="/windows/desktop/api/http/ne-http-http_response_info_type">HTTP_RESPONSE_INFO_TYPE</a> enumeration specifying the type of information contained in this structure.

### -field Length

The length, in bytes, of the <b>pInfo</b> member.

### -field pInfo

A pointer to the <a href="/windows/desktop/api/http/ns-http-http_multiple_known_headers">HTTP_MULTIPLE_KNOWN_HEADERS</a> structure when the <b>InfoType</b> member is <b>HttpResponseInfoTypeMultipleKnownHeaders</b>; otherwise <b>NULL</b>.

## -remarks

Starting with the HTTP Server API version 2.0, the HTTP_RESPONSE structure is extended to include an array of <b>HTTP_RESPONSE_INFO</b> structures in the <b>pRequestInfo</b> member. These structures contain additional information for the  response.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/ns-http-http_response_v2">HTTP_RESPONSE_V2</a>