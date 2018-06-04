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

# _HTTP_REQUEST_INFO_TYPE enumeration


## -description


The <b>HTTP_REQUEST_INFO_TYPE</b> enumeration defines the type of information contained in the <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structure. 

This enumeration is used  in the <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structure.


## -enum-fields




### -field HttpRequestInfoTypeAuth

The request information type is authentication.

The <b>pInfo</b> member of the <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structure points to a <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure.


### -field HttpRequestInfoTypeChannelBind


### -field HttpRequestInfoTypeSslProtocol


### -field HttpRequestInfoTypeSslTokenBindingDraft


### -field HttpRequestInfoTypeSslTokenBinding




## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a>
 

 

