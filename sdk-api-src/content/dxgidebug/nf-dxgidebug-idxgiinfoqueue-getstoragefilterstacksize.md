---
UID: NF:dxgidebug.IDXGIInfoQueue.GetStorageFilterStackSize
title: IDXGIInfoQueue::GetStorageFilterStackSize (dxgidebug.h)
description: Gets the size of the storage-filter stack in bytes.
helpviewer_keywords: ["GetStorageFilterStackSize","GetStorageFilterStackSize method [DXGI]","GetStorageFilterStackSize method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetStorageFilterStackSize method","IDXGIInfoQueue.GetStorageFilterStackSize","IDXGIInfoQueue::GetStorageFilterStackSize","direct3ddxgi.idxgiinfoqueue_getstoragefilterstacksize","dxgidebug/IDXGIInfoQueue::GetStorageFilterStackSize"]
old-location: direct3ddxgi\idxgiinfoqueue_getstoragefilterstacksize.htm
tech.root: direct3ddxgi
ms.assetid: FE4D1749-7587-48BA-9701-B09DDFF1CE84
ms.date: 12/05/2018
ms.keywords: GetStorageFilterStackSize, GetStorageFilterStackSize method [DXGI], GetStorageFilterStackSize method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetStorageFilterStackSize method, IDXGIInfoQueue.GetStorageFilterStackSize, IDXGIInfoQueue::GetStorageFilterStackSize, direct3ddxgi.idxgiinfoqueue_getstoragefilterstacksize, dxgidebug/IDXGIInfoQueue::GetStorageFilterStackSize
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
 - IDXGIInfoQueue::GetStorageFilterStackSize
 - dxgidebug/IDXGIInfoQueue::GetStorageFilterStackSize
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
 - IDXGIInfoQueue.GetStorageFilterStackSize
---

# IDXGIInfoQueue::GetStorageFilterStackSize


## -description

Gets the size of the storage-filter stack in bytes.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the size.

## -returns

Returns the size of the storage-filter stack in bytes.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>