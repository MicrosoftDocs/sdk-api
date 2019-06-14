---
UID: NF:dxgidebug.IDXGIInfoQueue.AddRetrievalFilterEntries
title: IDXGIInfoQueue::AddRetrievalFilterEntries (dxgidebug.h)
author: windows-sdk-content
description: Adds retrieval filters to the top of the retrieval-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_addretrievalfilterentries.htm
tech.root: direct3ddxgi
ms.assetid: D93CB421-6684-4E84-B7FF-7911496078CC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRetrievalFilterEntries, AddRetrievalFilterEntries method [DXGI], AddRetrievalFilterEntries method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddRetrievalFilterEntries method, IDXGIInfoQueue.AddRetrievalFilterEntries, IDXGIInfoQueue::AddRetrievalFilterEntries, direct3ddxgi.idxgiinfoqueue_addretrievalfilterentries, dxgidebug/IDXGIInfoQueue::AddRetrievalFilterEntries
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.AddRetrievalFilterEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIInfoQueue::AddRetrievalFilterEntries


## -description


Adds retrieval filters to the top of the retrieval-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that produced the filters.


### -param pFilter [in]

An array of <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter">DXGI_INFO_QUEUE_FILTER</a> structures that describe the filters.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
 

 

