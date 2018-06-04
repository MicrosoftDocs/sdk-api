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

# IWdsTransportMulticastSessionPolicy::put_SlowClientFallback


## -description


Receives  a value that indicates the fallback policy requested by the server when automatically disconnecting slow clients from a multicast transmission. A value of <b>VARIANT_FALSE</b> requests that the client disconnect from the server and discontinue any further attempts to get the content from this server. A value of <b>VARIANT_TRUE</b> requests that the client use any alternative method available to the client to get the content, for example  unicasting. 

This property can be used to get or set the fallback policy regardless of which method the server is using to handle  slow clients.

This policy is only used when the server is automatically disconnecting a slow client from a multicast transmission. An administrator  manually disconnecting a client, can specify the fallback method.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/bb6677d6-7c60-486a-825a-bafec1f3ffed">IWdsTransportMulticastSessionPolicy</a>
 

 

