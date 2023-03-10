---
UID: NF:dxgidebug.IDXGIInfoQueue.PopStorageFilter
title: IDXGIInfoQueue::PopStorageFilter (dxgidebug.h)
description: Pops a storage filter from the top of the storage-filter stack.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","PopStorageFilter method","IDXGIInfoQueue.PopStorageFilter","IDXGIInfoQueue::PopStorageFilter","PopStorageFilter","PopStorageFilter method [DXGI]","PopStorageFilter method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_popstoragefilter","dxgidebug/IDXGIInfoQueue::PopStorageFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_popstoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: B621336B-9334-4408-988F-6F5DBB2C4B53
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],PopStorageFilter method, IDXGIInfoQueue.PopStorageFilter, IDXGIInfoQueue::PopStorageFilter, PopStorageFilter, PopStorageFilter method [DXGI], PopStorageFilter method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_popstoragefilter, dxgidebug/IDXGIInfoQueue::PopStorageFilter
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
 - IDXGIInfoQueue::PopStorageFilter
 - dxgidebug/IDXGIInfoQueue::PopStorageFilter
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
 - IDXGIInfoQueue.PopStorageFilter
---

# IDXGIInfoQueue::PopStorageFilter


## -description

Pops a storage filter from the top of the storage-filter stack.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that pops the filter.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>