---
UID: NS:http._HTTP_REQUEST_INFO
title: HTTP_REQUEST_INFO (http.h)
description: Extends the HTTP_REQUEST structure with additional information about the request.
helpviewer_keywords: ["*PHTTP_REQUEST_INFO","*PHTTP_REQUEST_INFO structure [HTTP]","HTTP_REQUEST_INFO","HTTP_REQUEST_INFO structure [HTTP]","http.http_request_info","http/*PHTTP_REQUEST_INFO","http/HTTP_REQUEST_INFO"]
old-location: http\http_request_info.htm
tech.root: http
ms.assetid: 83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST_INFO, *PHTTP_REQUEST_INFO structure [HTTP], HTTP_REQUEST_INFO, HTTP_REQUEST_INFO structure [HTTP], http.http_request_info, http/*PHTTP_REQUEST_INFO, http/HTTP_REQUEST_INFO'
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
req.typenames: HTTP_REQUEST_INFO, *PHTTP_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_INFO
 - http/_HTTP_REQUEST_INFO
 - PHTTP_REQUEST_INFO
 - http/PHTTP_REQUEST_INFO
 - HTTP_REQUEST_INFO
 - http/HTTP_REQUEST_INFO
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
 - HTTP_REQUEST_INFO
---

# HTTP_REQUEST_INFO structure


## -description

The <b>HTTP_REQUEST_INFO</b> structure extends the <a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure with additional information about the request.

## -struct-fields

### -field InfoType

A member of the <a href="/windows/desktop/api/http/ne-http-http_request_info_type">HTTP_REQUEST_INFO_TYPE</a> enumeration specifying the type of information contained in this structure.

### -field InfoLength

The length, in bytes,  of the <b>pInfo</b> member.

### -field pInfo

A pointer to the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure when the <b>InfoType</b> member is <b>HttpRequestInfoTypeAuth</b>; otherwise <b>NULL</b>.

## -remarks

Starting with the HTTP Server API version 2.0, the HTTP_REQUEST structure is extended to include an array of <b>HTTP_REQUEST_INFO</b> structures in the <b>pRequestInfo</b> member. These structures contain additional information for the  request.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a>



<a href="/windows/desktop/api/http/ns-http-http_request_v2">HTTP_REQUEST_V2</a>