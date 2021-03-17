---
UID: NF:dxgidebug.IDXGIInfoQueue.GetRetrievalFilter
title: IDXGIInfoQueue::GetRetrievalFilter (dxgidebug.h)
description: Gets the retrieval filter at the top of the retrieval-filter stack.
helpviewer_keywords: ["GetRetrievalFilter","GetRetrievalFilter method [DXGI]","GetRetrievalFilter method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetRetrievalFilter method","IDXGIInfoQueue.GetRetrievalFilter","IDXGIInfoQueue::GetRetrievalFilter","direct3ddxgi.idxgiinfoqueue_getretrievalfilter","dxgidebug/IDXGIInfoQueue::GetRetrievalFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_getretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: 95907EF0-858B-4CDF-A112-6E59138769BD
ms.date: 12/05/2018
ms.keywords: GetRetrievalFilter, GetRetrievalFilter method [DXGI], GetRetrievalFilter method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetRetrievalFilter method, IDXGIInfoQueue.GetRetrievalFilter, IDXGIInfoQueue::GetRetrievalFilter, direct3ddxgi.idxgiinfoqueue_getretrievalfilter, dxgidebug/IDXGIInfoQueue::GetRetrievalFilter
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
 - IDXGIInfoQueue::GetRetrievalFilter
 - dxgidebug/IDXGIInfoQueue::GetRetrievalFilter
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
 - IDXGIInfoQueue.GetRetrievalFilter
---

# IDXGIInfoQueue::GetRetrievalFilter


## -description

Gets the retrieval filter at the top of the retrieval-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the filter.

### -param pFilter [out, optional]

A pointer to a <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_filter">DXGI_INFO_QUEUE_FILTER</a> structure that describes the filter.

### -param pFilterByteLength [in, out]

A pointer to a variable that receives the size, in bytes, of the filter description to which <i>pFilter</i> points. If <i>pFilter</i> is <b>NULL</b>, <b>GetRetrievalFilter</b> outputs the size of the retrieval filter.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>