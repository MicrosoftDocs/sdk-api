---
UID: NE:http._HTTP_RESPONSE_INFO_TYPE
title: HTTP_RESPONSE_INFO_TYPE (http.h)
description: The HTTP_RESPONSE_INFO_TYPE enumeration defines the type of information contained in the HTTP_RESPONSE_INFO structure.This enumeration is used in the HTTP_RESPONSE_INFO structure.
helpviewer_keywords: ["*PHTTP_RESPONSE_INFO_TYPE","*PHTTP_RESPONSE_INFO_TYPE enumeration [HTTP]","HTTP_RESPONSE_INFO_TYPE","HTTP_RESPONSE_INFO_TYPE enumeration [HTTP]","HttpResponseInfoTypeAuthenticationProperty","HttpResponseInfoTypeChannelBind","HttpResponseInfoTypeMultipleKnownHeaders","HttpResponseInfoTypeQosProperty","PHTTP_RESPONSE_INFO_TYPE","http.http_response_info_type","http/*PHTTP_RESPONSE_INFO_TYPE","http/HTTP_RESPONSE_INFO_TYPE","http/HttpResponseInfoTypeAuthenticationProperty","http/HttpResponseInfoTypeChannelBind","http/HttpResponseInfoTypeMultipleKnownHeaders","http/HttpResponseInfoTypeQosProperty"]
old-location: http\http_response_info_type.htm
tech.root: http
ms.assetid: 2f85e8dd-1693-4a54-a38f-9b70b2a46361
ms.date: 12/05/2018
ms.keywords: '*PHTTP_RESPONSE_INFO_TYPE, *PHTTP_RESPONSE_INFO_TYPE enumeration [HTTP], HTTP_RESPONSE_INFO_TYPE, HTTP_RESPONSE_INFO_TYPE enumeration [HTTP], HttpResponseInfoTypeAuthenticationProperty, HttpResponseInfoTypeChannelBind, HttpResponseInfoTypeMultipleKnownHeaders, HttpResponseInfoTypeQosProperty, PHTTP_RESPONSE_INFO_TYPE, http.http_response_info_type, http/*PHTTP_RESPONSE_INFO_TYPE, http/HTTP_RESPONSE_INFO_TYPE, http/HttpResponseInfoTypeAuthenticationProperty, http/HttpResponseInfoTypeChannelBind, http/HttpResponseInfoTypeMultipleKnownHeaders, http/HttpResponseInfoTypeQosProperty'
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
req.typenames: HTTP_RESPONSE_INFO_TYPE, PHTTP_RESPONSE_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_RESPONSE_INFO_TYPE
 - http/_HTTP_RESPONSE_INFO_TYPE
 - HTTP_RESPONSE_INFO_TYPE
 - http/HTTP_RESPONSE_INFO_TYPE
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
 - HTTP_RESPONSE_INFO_TYPE
---

## -description

The <b>HTTP_RESPONSE_INFO_TYPE</b> enumeration defines the type of information contained in the <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structure.

This enumeration is used  in the <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structure.

## -enum-fields

### -field HttpResponseInfoTypeMultipleKnownHeaders

The response information type is authentication.

The <b>pInfo</b> member of the <a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a> structure points to a <a href="/windows/desktop/api/http/ns-http-http_multiple_known_headers">HTTP_MULTIPLE_KNOWN_HEADERS</a> structure.

### -field HttpResponseInfoTypeAuthenticationProperty

Reserved for future use.

### -field HttpResponseInfoTypeQoSProperty

Pointer to an <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure that contains information about a QOS setting.

### -field HttpResponseInfoTypeChannelBind

Pointer to an <a href="/windows/desktop/api/http/ns-http-http_channel_bind_info">HTTP_CHANNEL_BIND_INFO</a> structure that contains information on the channel binding token.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="/windows/desktop/api/http/ns-http-http_response_info">HTTP_RESPONSE_INFO</a>