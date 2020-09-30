---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumMessagesDiscardedByMessageCountLimit
title: IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit (dxgidebug.h)
description: Gets the number of messages that were discarded due to the message count limit.
helpviewer_keywords: ["GetNumMessagesDiscardedByMessageCountLimit","GetNumMessagesDiscardedByMessageCountLimit method [DXGI]","GetNumMessagesDiscardedByMessageCountLimit method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetNumMessagesDiscardedByMessageCountLimit method","IDXGIInfoQueue.GetNumMessagesDiscardedByMessageCountLimit","IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit","direct3ddxgi.idxgiinfoqueue_getnummessagesdiscardedbymessagecountlimit","dxgidebug/IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit"]
old-location: direct3ddxgi\idxgiinfoqueue_getnummessagesdiscardedbymessagecountlimit.htm
tech.root: direct3ddxgi
ms.assetid: 8F97E69B-5534-409F-9702-9FC6D7940D65
ms.date: 12/05/2018
ms.keywords: GetNumMessagesDiscardedByMessageCountLimit, GetNumMessagesDiscardedByMessageCountLimit method [DXGI], GetNumMessagesDiscardedByMessageCountLimit method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumMessagesDiscardedByMessageCountLimit method, IDXGIInfoQueue.GetNumMessagesDiscardedByMessageCountLimit, IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit, direct3ddxgi.idxgiinfoqueue_getnummessagesdiscardedbymessagecountlimit, dxgidebug/IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit
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
 - IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit
 - dxgidebug/IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit
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
 - IDXGIInfoQueue.GetNumMessagesDiscardedByMessageCountLimit
---

# IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit


## -description

Gets the number of messages that were discarded due to the message count limit.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the number of messages that were discarded.

## -remarks

Get and set the message count limit with <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmessagecountlimit">IDXGIInfoQueue::GetMessageCountLimit</a> and <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setmessagecountlimit">IDXGIInfoQueue::SetMessageCountLimit</a>, respectively.



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>