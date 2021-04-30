---
UID: NF:dxgidebug.IDXGIInfoQueue.PopRetrievalFilter
title: IDXGIInfoQueue::PopRetrievalFilter (dxgidebug.h)
description: Pops a retrieval filter from the top of the retrieval-filter stack.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","PopRetrievalFilter method","IDXGIInfoQueue.PopRetrievalFilter","IDXGIInfoQueue::PopRetrievalFilter","PopRetrievalFilter","PopRetrievalFilter method [DXGI]","PopRetrievalFilter method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_popretrievalfilter","dxgidebug/IDXGIInfoQueue::PopRetrievalFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_popretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: E766B599-1168-4E8C-9433-0200D34CD38D
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PopRetrievalFilter method, IDXGIInfoQueue.PopRetrievalFilter, IDXGIInfoQueue::PopRetrievalFilter, PopRetrievalFilter, PopRetrievalFilter method [DXGI], PopRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_popretrievalfilter, dxgidebug/IDXGIInfoQueue::PopRetrievalFilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIInfoQueue::PopRetrievalFilter
 - dxgidebug/IDXGIInfoQueue::PopRetrievalFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.PopRetrievalFilter
---

# IDXGIInfoQueue::PopRetrievalFilter


## -description

Pops a retrieval filter from the top of the retrieval-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pops the filter.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>