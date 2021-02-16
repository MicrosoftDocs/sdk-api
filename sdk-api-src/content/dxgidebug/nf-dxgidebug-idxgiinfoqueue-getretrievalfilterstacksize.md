---
UID: NF:dxgidebug.IDXGIInfoQueue.GetRetrievalFilterStackSize
title: IDXGIInfoQueue::GetRetrievalFilterStackSize (dxgidebug.h)
description: Gets the size of the retrieval-filter stack in bytes.
helpviewer_keywords: ["GetRetrievalFilterStackSize","GetRetrievalFilterStackSize method [DXGI]","GetRetrievalFilterStackSize method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetRetrievalFilterStackSize method","IDXGIInfoQueue.GetRetrievalFilterStackSize","IDXGIInfoQueue::GetRetrievalFilterStackSize","direct3ddxgi.idxgiinfoqueue_getretrievalfilterstacksize","dxgidebug/IDXGIInfoQueue::GetRetrievalFilterStackSize"]
old-location: direct3ddxgi\idxgiinfoqueue_getretrievalfilterstacksize.htm
tech.root: direct3ddxgi
ms.assetid: E5173EC8-483D-4A90-BDF0-7A7D115A0CF9
ms.date: 12/05/2018
ms.keywords: GetRetrievalFilterStackSize, GetRetrievalFilterStackSize method [DXGI], GetRetrievalFilterStackSize method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetRetrievalFilterStackSize method, IDXGIInfoQueue.GetRetrievalFilterStackSize, IDXGIInfoQueue::GetRetrievalFilterStackSize, direct3ddxgi.idxgiinfoqueue_getretrievalfilterstacksize, dxgidebug/IDXGIInfoQueue::GetRetrievalFilterStackSize
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
 - IDXGIInfoQueue::GetRetrievalFilterStackSize
 - dxgidebug/IDXGIInfoQueue::GetRetrievalFilterStackSize
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
 - IDXGIInfoQueue.GetRetrievalFilterStackSize
---

# IDXGIInfoQueue::GetRetrievalFilterStackSize


## -description

Gets the size of the retrieval-filter stack in bytes.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the size.

## -returns

Returns the size of the retrieval-filter stack in bytes.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>