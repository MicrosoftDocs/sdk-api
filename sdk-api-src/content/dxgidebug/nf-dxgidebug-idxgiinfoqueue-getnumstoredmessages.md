---
UID: NF:dxgidebug.IDXGIInfoQueue.GetNumStoredMessages
title: IDXGIInfoQueue::GetNumStoredMessages (dxgidebug.h)
description: Gets the number of messages currently stored in the message queue.
helpviewer_keywords: ["GetNumStoredMessages","GetNumStoredMessages method [DXGI]","GetNumStoredMessages method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetNumStoredMessages method","IDXGIInfoQueue.GetNumStoredMessages","IDXGIInfoQueue::GetNumStoredMessages","direct3ddxgi.idxgiinfoqueue_getnumstoredmessages","dxgidebug/IDXGIInfoQueue::GetNumStoredMessages"]
old-location: direct3ddxgi\idxgiinfoqueue_getnumstoredmessages.htm
tech.root: direct3ddxgi
ms.assetid: 81556BB3-D8B8-4868-8B21-C9E01C3F183E
ms.date: 12/05/2018
ms.keywords: GetNumStoredMessages, GetNumStoredMessages method [DXGI], GetNumStoredMessages method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetNumStoredMessages method, IDXGIInfoQueue.GetNumStoredMessages, IDXGIInfoQueue::GetNumStoredMessages, direct3ddxgi.idxgiinfoqueue_getnumstoredmessages, dxgidebug/IDXGIInfoQueue::GetNumStoredMessages
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
 - IDXGIInfoQueue::GetNumStoredMessages
 - dxgidebug/IDXGIInfoQueue::GetNumStoredMessages
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
 - IDXGIInfoQueue.GetNumStoredMessages
---

# IDXGIInfoQueue::GetNumStoredMessages


## -description

Gets the number of messages currently stored in the message queue.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the number.

## -returns

Returns the number of messages currently stored in the message queue.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>