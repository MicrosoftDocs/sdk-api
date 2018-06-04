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

# IAMGraphBuilderCallback::SelectedFilter


## -description



The Filter Graph Manager calls this method when it finds a candidate filter for the graph, but before it creates the filter.




## -parameters




### -param pMon

Pointer to a moniker that contains information about the filter.


## -returns



If the method returns a success code, the Filter Graph Manager creates the filter and tries to connect it. If the method returns a failure code, the Filter Graph Manager rejects the filter.




## -remarks



This method enables the client to examine a filter to determine whether it is acceptable for the current filter graph.

The Filter Graph Manager holds a graph-wide critical section while it calls this method. Therefore, the callback method should avoid calling any methods on the Filter Graph Manager, or any methods on filters that might change the graph state (such as disconnecting pins). Doing so might cause a deadlock or other unexpected behaviors.




## -see-also




<a href="https://msdn.microsoft.com/4d8e45e3-7144-44ad-b79e-5acc0cec6ed4">IAMGraphBuilderCallback Interface</a>
 

 

