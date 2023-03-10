---
UID: NF:dxgidebug.IDXGIInfoQueue.PushRetrievalFilter
title: IDXGIInfoQueue::PushRetrievalFilter (dxgidebug.h)
description: Pushes a retrieval filter onto the retrieval-filter stack.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","PushRetrievalFilter method","IDXGIInfoQueue.PushRetrievalFilter","IDXGIInfoQueue::PushRetrievalFilter","PushRetrievalFilter","PushRetrievalFilter method [DXGI]","PushRetrievalFilter method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_pushretrievalfilter","dxgidebug/IDXGIInfoQueue::PushRetrievalFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_pushretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: 8027801C-ACDD-457D-A7A5-200B818D40A7
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushRetrievalFilter method, IDXGIInfoQueue.PushRetrievalFilter, IDXGIInfoQueue::PushRetrievalFilter, PushRetrievalFilter, PushRetrievalFilter method [DXGI], PushRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushretrievalfilter, dxgidebug/IDXGIInfoQueue::PushRetrievalFilter
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
 - IDXGIInfoQueue::PushRetrievalFilter
 - dxgidebug/IDXGIInfoQueue::PushRetrievalFilter
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
 - IDXGIInfoQueue.PushRetrievalFilter
---

# IDXGIInfoQueue::PushRetrievalFilter


## -description

Pushes a retrieval filter onto the retrieval-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the filter.

### -param pFilter [in]

A pointer to a <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter">DXGI_INFO_QUEUE_FILTER</a> structure that describes the filter.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>