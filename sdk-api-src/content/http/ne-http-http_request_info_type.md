---
UID: NE:http._HTTP_REQUEST_INFO_TYPE
title: HTTP_REQUEST_INFO_TYPE (http.h)
description: The HTTP_REQUEST_INFO_TYPE enumeration defines the type of information contained in the HTTP_REQUEST_INFO structure. This enumeration is used in the HTTP_REQUEST_INFO structure.
helpviewer_keywords: ["*PHTTP_REQUEST_INFO_TYPE","*PHTTP_REQUEST_INFO_TYPE enumeration [HTTP]","HTTP_REQUEST_INFO_TYPE","HTTP_REQUEST_INFO_TYPE enumeration [HTTP]","HttpRequestInfoTypeAuth","http.http_request_info_type","http/*PHTTP_REQUEST_INFO_TYPE","http/HTTP_REQUEST_INFO_TYPE","http/HttpRequestInfoTypeAuth"]
old-location: http\http_request_info_type.htm
tech.root: http
ms.assetid: 178d2608-85c8-4842-bd6a-4c66d7f1b892
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST_INFO_TYPE, *PHTTP_REQUEST_INFO_TYPE enumeration [HTTP], HTTP_REQUEST_INFO_TYPE, HTTP_REQUEST_INFO_TYPE enumeration [HTTP], HttpRequestInfoTypeAuth, http.http_request_info_type, http/*PHTTP_REQUEST_INFO_TYPE, http/HTTP_REQUEST_INFO_TYPE, http/HttpRequestInfoTypeAuth'
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
req.typenames: HTTP_REQUEST_INFO_TYPE, *PHTTP_REQUEST_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_INFO_TYPE
 - http/_HTTP_REQUEST_INFO_TYPE
 - PHTTP_REQUEST_INFO_TYPE
 - http/PHTTP_REQUEST_INFO_TYPE
 - HTTP_REQUEST_INFO_TYPE
 - http/HTTP_REQUEST_INFO_TYPE
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
 - HTTP_REQUEST_INFO_TYPE
---

# HTTP_REQUEST_INFO_TYPE enumeration


## -description

The <b>HTTP_REQUEST_INFO_TYPE</b> enumeration defines the type of information contained in the <a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a> structure. 

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a> structure.

## -enum-fields

### -field HttpRequestInfoTypeAuth

The request information type is authentication.

The <b>pInfo</b> member of the <a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a> structure points to a <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure.

### -field HttpRequestInfoTypeChannelBind

### -field HttpRequestInfoTypeSslProtocol

### -field HttpRequestInfoTypeSslTokenBindingDraft

### -field HttpRequestInfoTypeSslTokenBinding

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_request_info">HTTP_REQUEST_INFO</a>