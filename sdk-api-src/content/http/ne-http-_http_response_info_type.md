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
 

 

