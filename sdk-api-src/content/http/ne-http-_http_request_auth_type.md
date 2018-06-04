---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _HTTP_REQUEST_AUTH_TYPE enumeration


## -description


The <b>HTTP_REQUEST_AUTH_TYPE</b> enumeration defines the authentication types supported by the HTTP Server API.

This enumeration is used  in the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure.


## -enum-fields




### -field HttpRequestAuthTypeNone

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




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a>
 

 

