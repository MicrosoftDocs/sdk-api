---
UID: NE:http._HTTP_RESPONSE_INFO_TYPE
title: "_HTTP_RESPONSE_INFO_TYPE"
author: windows-sdk-content
description: The HTTP_RESPONSE_INFO_TYPE enumeration defines the type of information contained in the HTTP_RESPONSE_INFO structure.This enumeration is used in the HTTP_RESPONSE_INFO structure.
old-location: http\http_response_info_type.htm
tech.root: http
ms.assetid: 2f85e8dd-1693-4a54-a38f-9b70b2a46361
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PHTTP_RESPONSE_INFO_TYPE, *PHTTP_RESPONSE_INFO_TYPE enumeration [HTTP], HTTP_RESPONSE_INFO_TYPE, HTTP_RESPONSE_INFO_TYPE enumeration [HTTP], HttpResponseInfoTypeAuthenticationProperty, HttpResponseInfoTypeChannelBind, HttpResponseInfoTypeMultipleKnownHeaders, HttpResponseInfoTypeQosProperty, PHTTP_RESPONSE_INFO_TYPE, _HTTP_RESPONSE_INFO_TYPE, http.http_response_info_type, http/*PHTTP_RESPONSE_INFO_TYPE, http/HTTP_RESPONSE_INFO_TYPE, http/HttpResponseInfoTypeAuthenticationProperty, http/HttpResponseInfoTypeChannelBind, http/HttpResponseInfoTypeMultipleKnownHeaders, http/HttpResponseInfoTypeQosProperty"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_RESPONSE_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: HTTP_RESPONSE_INFO_TYPE, PHTTP_RESPONSE_INFO_TYPE
req.redist: 
---

# _HTTP_RESPONSE_INFO_TYPE enumeration


## -description


The <b>HTTP_RESPONSE_INFO_TYPE</b> enumeration defines the type of information contained in the <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structure.

This enumeration is used  in the <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structure.


## -enum-fields




### -field HttpResponseInfoTypeMultipleKnownHeaders

The response information type is authentication.

The <b>pInfo</b> member of the <a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a> structure points to a <a href="https://msdn.microsoft.com/b5e68d55-43a4-422f-b7e3-163739628720">HTTP_MULTIPLE_KNOWN_HEADERS</a> structure.


### -field HttpResponseInfoTypeAuthenticationProperty

Reserved for future use.


### -field HttpResponseInfoTypeQoSProperty


### -field HttpResponseInfoTypeChannelBind

Pointer to an <a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a> structure that contains information on the channel binding token.


#### - HttpResponseInfoTypeQosProperty

Pointer to an <a href="https://msdn.microsoft.com/6c220063-02d0-44c0-b3a3-e7bfd5c57e1f">HTTP_QOS_SETTING_INFO</a> structure that contains information about a QOS setting.


## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/29422116-0a33-4553-98aa-785bb926dee0">HTTP_RESPONSE_INFO</a>
 

 

