---
UID: NS:traffic._IPX_PATTERN
title: "_IPX_PATTERN"
author: windows-sdk-content
description: The IPX_PATTERN structure applies a specific pattern or corresponding mask for the IPX protocol. The IPX_PATTERN structure designation is used by the traffic control interface in the application of packet filters.
old-location: qos\ipx_pattern.htm
old-project: QOS
ms.assetid: bbb5466c-3ec4-48a7-a50e-4859d074d001
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*PIPX_PATTERN, *PIPX_PATTERN structure [QOS], IPX_PATTERN, IPX_PATTERN structure [QOS], _IPX_PATTERN, qos.ipx_pattern, traffic/*PIPX_PATTERN, traffic/IPX_PATTERN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IPX_PATTERN, *PIPX_PATTERN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Traffic.h
api_name:
-	IPX_PATTERN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

