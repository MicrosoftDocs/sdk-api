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

# PeerFreeData function


## -description



      The <b>PeerFreeData</b> function deallocates a block of data and returns it to the memory pool. Use the <b>PeerFreeData</b> function to free  data that the Peer Identity Manager, Peer Grouping, and Peer Collaboration APIs return. 


## -parameters




### -param pvData [in]

Pointer to a block of data to be deallocated. This parameter must reference a valid block of memory.


## -returns



There are no return values.




## -remarks



Do not use this function to release memory that the Peer Graphing API returns. Use <a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a> for memory that  the Peer Graphing API returns.




## -see-also




<a href="https://msdn.microsoft.com/56ea2880-b468-4816-b6c9-5780c807b3f1">Grouping API
		  Functions</a>



<a href="https://msdn.microsoft.com/7621d26b-92e3-40c9-b0ce-94647d67f2c4">Identity Manager Functions</a>
 

 

