---
UID: NF:dxgidebug.IDXGIInfoQueue.PushDenyAllRetrievalFilter
title: IDXGIInfoQueue::PushDenyAllRetrievalFilter (dxgidebug.h)
description: Pushes a deny-all retrieval filter onto the retrieval-filter stack.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","PushDenyAllRetrievalFilter method","IDXGIInfoQueue.PushDenyAllRetrievalFilter","IDXGIInfoQueue::PushDenyAllRetrievalFilter","PushDenyAllRetrievalFilter","PushDenyAllRetrievalFilter method [DXGI]","PushDenyAllRetrievalFilter method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_pushdenyallretrievalfilter","dxgidebug/IDXGIInfoQueue::PushDenyAllRetrievalFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_pushdenyallretrievalfilter.htm
tech.root: direct3ddxgi
ms.assetid: 104C5BAD-D1FF-47EC-A1FA-C4B32EA4DFB6
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushDenyAllRetrievalFilter method, IDXGIInfoQueue.PushDenyAllRetrievalFilter, IDXGIInfoQueue::PushDenyAllRetrievalFilter, PushDenyAllRetrievalFilter, PushDenyAllRetrievalFilter method [DXGI], PushDenyAllRetrievalFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushdenyallretrievalfilter, dxgidebug/IDXGIInfoQueue::PushDenyAllRetrievalFilter
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
 - IDXGIInfoQueue::PushDenyAllRetrievalFilter
 - dxgidebug/IDXGIInfoQueue::PushDenyAllRetrievalFilter
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
 - IDXGIInfoQueue.PushDenyAllRetrievalFilter
---

# IDXGIInfoQueue::PushDenyAllRetrievalFilter


## -description

Pushes a deny-all retrieval filter onto the retrieval-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the deny-all retrieval filter.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

A deny-all retrieval filter prevents all messages from passing through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>