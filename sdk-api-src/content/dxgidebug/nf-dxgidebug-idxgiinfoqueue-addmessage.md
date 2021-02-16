---
UID: NF:dxgidebug.IDXGIInfoQueue.AddMessage
title: IDXGIInfoQueue::AddMessage (dxgidebug.h)
description: Adds a debug message to the message queue and sends that message to the debug output.
helpviewer_keywords: ["AddMessage","AddMessage method [DXGI]","AddMessage method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","AddMessage method","IDXGIInfoQueue.AddMessage","IDXGIInfoQueue::AddMessage","direct3ddxgi.idxgiinfoqueue_addmessage","dxgidebug/IDXGIInfoQueue::AddMessage"]
old-location: direct3ddxgi\idxgiinfoqueue_addmessage.htm
tech.root: direct3ddxgi
ms.assetid: 965DA310-D082-4970-BCD1-F15F44C074D0
ms.date: 12/05/2018
ms.keywords: AddMessage, AddMessage method [DXGI], AddMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddMessage method, IDXGIInfoQueue.AddMessage, IDXGIInfoQueue::AddMessage, direct3ddxgi.idxgiinfoqueue_addmessage, dxgidebug/IDXGIInfoQueue::AddMessage
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
 - IDXGIInfoQueue::AddMessage
 - dxgidebug/IDXGIInfoQueue::AddMessage
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
 - IDXGIInfoQueue.AddMessage
---

# IDXGIInfoQueue::AddMessage


## -description

Adds a debug message to the message queue and sends that message to the debug output.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that produced the message.

### -param Category [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_category">DXGI_INFO_QUEUE_MESSAGE_CATEGORY</a>-typed value that specifies the category of the message.

### -param Severity [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.

### -param ID [in]

An integer that uniquely identifies the message.

### -param pDescription [in]

The message string.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>