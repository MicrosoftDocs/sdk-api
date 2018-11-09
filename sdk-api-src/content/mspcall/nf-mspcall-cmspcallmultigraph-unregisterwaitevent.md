---
UID: NF:mspcall.CMSPCallMultiGraph.UnregisterWaitEvent
title: CMSPCallMultiGraph::UnregisterWaitEvent
author: windows-sdk-content
description: The UnregisterWaitEvent method calls the UnregisterWait function to tell the thread pool to stop waiting on the handle indicated by the wait block at the given index.
old-location: tapi3\cmspcallmultigraph_unregisterwaitevent.htm
tech.root: tapi
ms.assetid: a6d20bb9-fa50-4627-a3de-886cde4b8911
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],UnregisterWaitEvent method, CMSPCallMultiGraph.UnregisterWaitEvent, CMSPCallMultiGraph::UnregisterWaitEvent, UnregisterWaitEvent, UnregisterWaitEvent method [TAPI 2.2], UnregisterWaitEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_unregisterwaitevent, mspcall/CMSPCallMultiGraph::UnregisterWaitEvent, tapi3.cmspcallmultigraph_unregisterwaitevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mspcall.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallMultiGraph.UnregisterWaitEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

