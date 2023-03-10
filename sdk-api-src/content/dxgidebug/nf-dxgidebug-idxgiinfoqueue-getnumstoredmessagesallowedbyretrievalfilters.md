---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters
title: IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters (dxgidebug.h)
description: Gets the number of messages that can pass through a retrieval filter.
helpviewer_keywords: ["GetNumStoredMessagesAllowedByRetrievalFilters","GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI]","GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetNumStoredMessagesAllowedByRetrievalFilters method","IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters","IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters","direct3ddxgi.idxgiinfoqueue_getnumstoredmessagesallowedbyretrievalfilters","dxgidebug/IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters"]
old-location: direct3ddxgi\idxgiinfoqueue_getnumstoredmessagesallowedbyretrievalfilters.htm
tech.root: direct3ddxgi
ms.assetid: 1BFFEE9F-7902-41B7-9607-BD0E955FBD8B
ms.date: 12/05/2018
ms.keywords: GetNumStoredMessagesAllowedByRetrievalFilters, GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI], GetNumStoredMessagesAllowedByRetrievalFilters method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumStoredMessagesAllowedByRetrievalFilters method, IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters, IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters, direct3ddxgi.idxgiinfoqueue_getnumstoredmessagesallowedbyretrievalfilters, dxgidebug/IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters
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
 - IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters
 - dxgidebug/IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters
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
 - IDXGIInfoQueue.GetNumStoredMessagesAllowedByRetrievalFilters
---

# IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters


## -description

Gets the number of messages that can pass through a retrieval filter.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the number of messages that can pass through a retrieval filter.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>