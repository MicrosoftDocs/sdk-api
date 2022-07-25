---
UID: NE:http._HTTP_REQUEST_AUTH_TYPE
title: HTTP_REQUEST_AUTH_TYPE (http.h)
description: The HTTP_REQUEST_AUTH_TYPE enumeration defines the authentication types supported by the HTTP Server API.This enumeration is used in the HTTP_REQUEST_AUTH_INFO structure.
helpviewer_keywords: ["*PHTTP_REQUEST_AUTH_TYPE","*PHTTP_REQUEST_AUTH_TYPE enumeration [HTTP]","HTTP_REQUEST_AUTH_TYPE","HTTP_REQUEST_AUTH_TYPE enumeration [HTTP]","HttpRequestAuthTypeBasic","HttpRequestAuthTypeDigest","HttpRequestAuthTypeKerberos","HttpRequestAuthTypeNTLM","HttpRequestAuthTypeNegotiate","HttpRequestAuthTypeNone","http.http_request_auth_type","http/*PHTTP_REQUEST_AUTH_TYPE","http/HTTP_REQUEST_AUTH_TYPE","http/HttpRequestAuthTypeBasic","http/HttpRequestAuthTypeDigest","http/HttpRequestAuthTypeKerberos","http/HttpRequestAuthTypeNTLM","http/HttpRequestAuthTypeNegotiate","http/HttpRequestAuthTypeNone"]
old-location: http\http_request_auth_type.htm
tech.root: http
ms.assetid: e0147da5-7de2-4ea8-abc5-61c814ee7c55
ms.date: 12/05/2018
ms.keywords: '*PHTTP_REQUEST_AUTH_TYPE, *PHTTP_REQUEST_AUTH_TYPE enumeration [HTTP], HTTP_REQUEST_AUTH_TYPE, HTTP_REQUEST_AUTH_TYPE enumeration [HTTP], HttpRequestAuthTypeBasic, HttpRequestAuthTypeDigest, HttpRequestAuthTypeKerberos, HttpRequestAuthTypeNTLM, HttpRequestAuthTypeNegotiate, HttpRequestAuthTypeNone, http.http_request_auth_type, http/*PHTTP_REQUEST_AUTH_TYPE, http/HTTP_REQUEST_AUTH_TYPE, http/HttpRequestAuthTypeBasic, http/HttpRequestAuthTypeDigest, http/HttpRequestAuthTypeKerberos, http/HttpRequestAuthTypeNTLM, http/HttpRequestAuthTypeNegotiate, http/HttpRequestAuthTypeNone'
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
req.typenames: HTTP_REQUEST_AUTH_TYPE, *PHTTP_REQUEST_AUTH_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_AUTH_TYPE
 - http/_HTTP_REQUEST_AUTH_TYPE
 - PHTTP_REQUEST_AUTH_TYPE
 - http/PHTTP_REQUEST_AUTH_TYPE
 - HTTP_REQUEST_AUTH_TYPE
 - http/HTTP_REQUEST_AUTH_TYPE
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
 - HTTP_REQUEST_AUTH_TYPE
---

# HTTP_REQUEST_AUTH_TYPE enumeration


## -description

The <b>HTTP_REQUEST_AUTH_TYPE</b> enumeration defines the authentication types supported by the HTTP Server API.

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a> structure.

## -enum-fields

### -field HttpRequestAuthTypeNone:0

No authentication is attempted for the request.

### -field HttpRequestAuthTypeBasic

Basic authentication is attempted for the request.

### -field HttpRequestAuthTypeDigest

 Digest authentication is attempted for the request.

### -field HttpRequestAuthTypeNTLM

 NTLM authentication is attempted for the request.

### -field HttpRequestAuthTypeNegotiate

 Negotiate authentication is attempted for the request.

### -field HttpRequestAuthTypeKerberos

Kerberos authentication is attempted for the request.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_request_auth_info">HTTP_REQUEST_AUTH_INFO</a>
