---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumMessagesDeniedByStorageFilter
title: IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter (dxgidebug.h)
description: Gets the number of messages that were denied passage through a storage filter.
helpviewer_keywords: ["GetNumMessagesDeniedByStorageFilter","GetNumMessagesDeniedByStorageFilter method [DXGI]","GetNumMessagesDeniedByStorageFilter method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetNumMessagesDeniedByStorageFilter method","IDXGIInfoQueue.GetNumMessagesDeniedByStorageFilter","IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter","direct3ddxgi.idxgiinfoqueue_getnummessagesdeniedbystoragefilter","dxgidebug/IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_getnummessagesdeniedbystoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: 98A71D07-8E9A-403D-B02B-70B7F4112246
ms.date: 12/05/2018
ms.keywords: GetNumMessagesDeniedByStorageFilter, GetNumMessagesDeniedByStorageFilter method [DXGI], GetNumMessagesDeniedByStorageFilter method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumMessagesDeniedByStorageFilter method, IDXGIInfoQueue.GetNumMessagesDeniedByStorageFilter, IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter, direct3ddxgi.idxgiinfoqueue_getnummessagesdeniedbystoragefilter, dxgidebug/IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter
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
 - IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter
 - dxgidebug/IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter
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
 - IDXGIInfoQueue.GetNumMessagesDeniedByStorageFilter
---

# IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter


## -description

Gets the number of messages that were denied passage through a storage filter.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the number of messages denied by a storage filter.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>