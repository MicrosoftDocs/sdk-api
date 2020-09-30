---
UID: NF:dxgidebug.IDXGIInfoQueue.PushEmptyStorageFilter
title: IDXGIInfoQueue::PushEmptyStorageFilter (dxgidebug.h)
description: Pushes an empty storage filter onto the storage-filter stack.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","PushEmptyStorageFilter method","IDXGIInfoQueue.PushEmptyStorageFilter","IDXGIInfoQueue::PushEmptyStorageFilter","PushEmptyStorageFilter","PushEmptyStorageFilter method [DXGI]","PushEmptyStorageFilter method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_pushemptystoragefilter","dxgidebug/IDXGIInfoQueue::PushEmptyStorageFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_pushemptystoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: C0DC43B8-4869-49B0-A4D9-6907BCF1CB9E
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PushEmptyStorageFilter method, IDXGIInfoQueue.PushEmptyStorageFilter, IDXGIInfoQueue::PushEmptyStorageFilter, PushEmptyStorageFilter, PushEmptyStorageFilter method [DXGI], PushEmptyStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_pushemptystoragefilter, dxgidebug/IDXGIInfoQueue::PushEmptyStorageFilter
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
 - IDXGIInfoQueue::PushEmptyStorageFilter
 - dxgidebug/IDXGIInfoQueue::PushEmptyStorageFilter
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
 - IDXGIInfoQueue.PushEmptyStorageFilter
---

# IDXGIInfoQueue::PushEmptyStorageFilter


## -description

Pushes an empty storage filter onto the storage-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pushes the empty storage filter.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

An empty storage filter allows all messages to pass through.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>