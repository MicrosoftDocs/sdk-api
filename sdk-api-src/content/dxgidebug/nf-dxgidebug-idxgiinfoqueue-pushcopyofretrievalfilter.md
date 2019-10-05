---
UID: NF:dxgidebug.IDXGIInfoQueue.PushCopyOfRetrievalFilter
title: IDXGIInfoQueue::PushCopyOfRetrievalFilter (dxgidebug.h)
author: windows-sdk-content
description: Pushes a copy of the retrieval filter that is currently on the top of the retrieval-filter stack onto the retrieval-filter stack.
old-location: direct3ddxgi\idxgiinfoqueue_pushcopyofretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: D1F82073-14DB-47B5-AB61-C1AFE5C50C42
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushCopyOfRetrievalFilter method, IDXGIInfoQueue.PushCopyOfRetrievalFilter, IDXGIInfoQueue::PushCopyOfRetrievalFilter, PushCopyOfRetrievalFilter, PushCopyOfRetrievalFilter method [DXGI], PushCopyOfRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushcopyofretrievalfilter, dxgidebug/IDXGIInfoQueue::PushCopyOfRetrievalFilter
ms.topic: method
f1_keywords: 
 - "dxgidebug/IDXGIInfoQueue.PushCopyOfRetrievalFilter"
dev_langs:
 - c++
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
 - IDXGIInfoQueue.PushCopyOfRetrievalFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIInfoQueue::PushCopyOfRetrievalFilter


## -description


Pushes a copy of the retrieval filter that is currently on the top of the retrieval-filter stack onto the retrieval-filter stack.


## -parameters




### -param Producer [in]

 A <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the copy of the retrieval filter.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
 

 

