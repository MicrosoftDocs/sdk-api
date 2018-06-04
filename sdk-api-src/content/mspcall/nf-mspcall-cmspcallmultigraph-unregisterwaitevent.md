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

# CMSPCallMultiGraph::UnregisterWaitEvent


## -description


The 
<b>UnregisterWaitEvent</b> method calls the <a href="https://msdn.microsoft.com/9ae8879f-0dbd-4d04-ae6e-094324f82acf">UnregisterWait</a> function 
to tell the thread pool to stop waiting on the handle indicated by the wait block at the given index. Releases the refcounts in the wait block and frees the wait block. Removes the wait block from the list of wait blocks.


## -parameters




### -param index

Index on appropriate item in the array of 
<a href="https://msdn.microsoft.com/cf7171f6-f51a-4089-9422-4a0e182926f1">THREADPOOLWAITBLOCK</a> structures.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

