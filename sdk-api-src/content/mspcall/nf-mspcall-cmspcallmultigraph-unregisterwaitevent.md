---
UID: NF:mspcall.CMSPCallMultiGraph.UnregisterWaitEvent
title: CMSPCallMultiGraph::UnregisterWaitEvent (mspcall.h)
description: The UnregisterWaitEvent method calls the UnregisterWait function to tell the thread pool to stop waiting on the handle indicated by the wait block at the given index.
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","UnregisterWaitEvent method","CMSPCallMultiGraph.UnregisterWaitEvent","CMSPCallMultiGraph::UnregisterWaitEvent","UnregisterWaitEvent","UnregisterWaitEvent method [TAPI 2.2]","UnregisterWaitEvent method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_unregisterwaitevent","mspcall/CMSPCallMultiGraph::UnregisterWaitEvent","tapi3.cmspcallmultigraph_unregisterwaitevent"]
old-location: tapi3\cmspcallmultigraph_unregisterwaitevent.htm
tech.root: tapi3
ms.assetid: a6d20bb9-fa50-4627-a3de-886cde4b8911
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],UnregisterWaitEvent method, CMSPCallMultiGraph.UnregisterWaitEvent, CMSPCallMultiGraph::UnregisterWaitEvent, UnregisterWaitEvent, UnregisterWaitEvent method [TAPI 2.2], UnregisterWaitEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_unregisterwaitevent, mspcall/CMSPCallMultiGraph::UnregisterWaitEvent, tapi3.cmspcallmultigraph_unregisterwaitevent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallMultiGraph::UnregisterWaitEvent
 - mspcall/CMSPCallMultiGraph::UnregisterWaitEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallMultiGraph.UnregisterWaitEvent
---

# CMSPCallMultiGraph::UnregisterWaitEvent


## -description

The 
<b>UnregisterWaitEvent</b> method calls the <a href="/windows/desktop/api/winbase/nf-winbase-unregisterwait">UnregisterWait</a> function 
to tell the thread pool to stop waiting on the handle indicated by the wait block at the given index. Releases the refcounts in the wait block and frees the wait block. Removes the wait block from the list of wait blocks.

## -parameters

### -param index

Index on appropriate item in the array of 
<a href="/previous-versions/windows/desktop/legacy/ms734804(v=vs.85)">THREADPOOLWAITBLOCK</a> structures.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>