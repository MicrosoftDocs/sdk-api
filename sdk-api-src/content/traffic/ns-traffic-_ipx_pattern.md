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

# _IPX_PATTERN structure


## -description


The <b>IPX_PATTERN</b> structure applies a specific pattern or corresponding mask for the IPX protocol. The 
<b>IPX_PATTERN</b> structure designation is used by the traffic control interface in the application of packet filters.


## -struct-fields




### -field Src

 


### -field Src.NetworkAddress

 


### -field Src.NodeAddress

 


### -field Src.Socket

 


### -field Dest

 




#### - Src, Dest

Structure used to contain source and destination address information for traffic flow.



#### NetworkAddress

IPX network address to which the node belongs.



#### NodeAddress

IPX  node address of the computer.



#### Socket

Socket on which the mask is to be applied.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

