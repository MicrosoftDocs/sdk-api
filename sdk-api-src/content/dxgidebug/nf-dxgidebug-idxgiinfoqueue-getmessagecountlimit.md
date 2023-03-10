---
UID: NF:dxgidebug.IDXGIInfoQueue.GetMessageCountLimit
title: IDXGIInfoQueue::GetMessageCountLimit (dxgidebug.h)
description: Gets the maximum number of messages that can be added to the message queue.
helpviewer_keywords: ["GetMessageCountLimit","GetMessageCountLimit method [DXGI]","GetMessageCountLimit method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetMessageCountLimit method","IDXGIInfoQueue.GetMessageCountLimit","IDXGIInfoQueue::GetMessageCountLimit","direct3ddxgi.idxgiinfoqueue_getmessagecountlimit","dxgidebug/IDXGIInfoQueue::GetMessageCountLimit"]
old-location: direct3ddxgi\idxgiinfoqueue_getmessagecountlimit.htm
tech.root: direct3ddxgi
ms.assetid: F9700374-255D-423E-8E60-4FE7FFA9E807
ms.date: 12/05/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method [DXGI], GetMessageCountLimit method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetMessageCountLimit method, IDXGIInfoQueue.GetMessageCountLimit, IDXGIInfoQueue::GetMessageCountLimit, direct3ddxgi.idxgiinfoqueue_getmessagecountlimit, dxgidebug/IDXGIInfoQueue::GetMessageCountLimit
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
 - IDXGIInfoQueue::GetMessageCountLimit
 - dxgidebug/IDXGIInfoQueue::GetMessageCountLimit
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
 - IDXGIInfoQueue.GetMessageCountLimit
---

# IDXGIInfoQueue::GetMessageCountLimit


## -description

Gets the maximum number of messages that can be added to the message queue.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the maximum number of messages that can be added to the queue. –1 means no limit.

## -remarks

When the number of messages in the message queue reaches the maximum limit, new messages coming in push old messages out.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>