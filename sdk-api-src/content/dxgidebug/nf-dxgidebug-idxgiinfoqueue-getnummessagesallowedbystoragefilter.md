---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumMessagesAllowedByStorageFilter
title: IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter (dxgidebug.h)
description: Gets the number of messages that a storage filter allowed to pass through.
helpviewer_keywords: ["GetNumMessagesAllowedByStorageFilter","GetNumMessagesAllowedByStorageFilter method [DXGI]","GetNumMessagesAllowedByStorageFilter method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetNumMessagesAllowedByStorageFilter method","IDXGIInfoQueue.GetNumMessagesAllowedByStorageFilter","IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter","direct3ddxgi.idxgiinfoqueue_getnummessagesallowedbystoragefilter","dxgidebug/IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter"]
old-location: direct3ddxgi\idxgiinfoqueue_getnummessagesallowedbystoragefilter.htm
tech.root: direct3ddxgi
ms.assetid: B838A0D9-6888-46BF-AE18-8C3546535037
ms.date: 12/05/2018
ms.keywords: GetNumMessagesAllowedByStorageFilter, GetNumMessagesAllowedByStorageFilter method [DXGI], GetNumMessagesAllowedByStorageFilter method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumMessagesAllowedByStorageFilter method, IDXGIInfoQueue.GetNumMessagesAllowedByStorageFilter, IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter, direct3ddxgi.idxgiinfoqueue_getnummessagesallowedbystoragefilter, dxgidebug/IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter
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
 - IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter
 - dxgidebug/IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter
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
 - IDXGIInfoQueue.GetNumMessagesAllowedByStorageFilter
---

# IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter


## -description

Gets the number of messages that a storage filter allowed to pass through.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the number of messages allowed by a storage filter.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>