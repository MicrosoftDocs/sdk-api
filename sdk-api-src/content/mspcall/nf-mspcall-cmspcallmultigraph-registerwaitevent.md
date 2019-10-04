---
UID: NF:mspcall.CMSPCallMultiGraph.RegisterWaitEvent
title: CMSPCallMultiGraph::RegisterWaitEvent (mspcall.h)
author: windows-sdk-content
description: The RegisterWaitEvent method should be called only within a critical section on the call object.
old-location: tapi3\cmspcallmultigraph_registerwaitevent.htm
tech.root: Tapi
ms.assetid: 3c75ed75-a0b2-435b-aa49-c1e7dadf260f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],RegisterWaitEvent method, CMSPCallMultiGraph.RegisterWaitEvent, CMSPCallMultiGraph::RegisterWaitEvent, RegisterWaitEvent, RegisterWaitEvent method [TAPI 2.2], RegisterWaitEvent method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_registerwaitevent, mspcall/CMSPCallMultiGraph::RegisterWaitEvent, tapi3.cmspcallmultigraph_registerwaitevent
ms.topic: method
f1_keywords: 
 - "mspcall/CMSPCallMultiGraph.RegisterWaitEvent"
dev_langs:
 - c++
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
 - CMSPCallMultiGraph.RegisterWaitEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPCallMultiGraph::RegisterWaitEvent


## -description


The 
<b>RegisterWaitEvent</b> method should be called only within a critical section on the call object. It allocates a thread pool context block, fills in the fields, increments the reference counts, and posts the block to the thread pool by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> function. Saves the wait handle returned for use in 
<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-unregisterwaitevent">UnregisterWaitEvent</a>. Saves the wait block in the list of wait blocks.


## -parameters




### -param pIMediaEvent

Pointer to DirectShow <b>IMediaEvent</b> interface.


### -param pITStream

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>
 

 

