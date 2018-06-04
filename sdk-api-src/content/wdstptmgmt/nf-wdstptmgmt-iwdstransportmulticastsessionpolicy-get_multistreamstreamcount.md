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

# IWdsTransportMulticastSessionPolicy::get_MultistreamStreamCount


## -description


Receives  the maximum number of multicast streams per transmission used by the server. If the server is configured to handle slow clients using the multistream method, the server detects clients that slow transmission below this maximum and moves them to lower-speed streams of the same multicast transmission.   The server cannot move legacy clients that do not support the multistream handling option, and in this case, the server disconnects the client or instructs the client to fallback depending upon the <a href="https://msdn.microsoft.com/cce0ba98-382a-45d5-8381-06864061c529">SlowClientFallback</a> property.

This property can be used to get or set the maximum stream count regardless of which method the server is using to handle  slow clients.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/bb6677d6-7c60-486a-825a-bafec1f3ffed">IWdsTransportMulticastSessionPolicy</a>
 

 

