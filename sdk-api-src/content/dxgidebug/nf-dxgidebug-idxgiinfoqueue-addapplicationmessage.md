---
UID: NF:dxgidebug.IDXGIInfoQueue.AddApplicationMessage
title: IDXGIInfoQueue::AddApplicationMessage (dxgidebug.h)
description: Adds a user-defined message to the message queue and sends that message to the debug output.
helpviewer_keywords: ["AddApplicationMessage","AddApplicationMessage method [DXGI]","AddApplicationMessage method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","AddApplicationMessage method","IDXGIInfoQueue.AddApplicationMessage","IDXGIInfoQueue::AddApplicationMessage","direct3ddxgi.idxgiinfoqueue_addapplicationmessage","dxgidebug/IDXGIInfoQueue::AddApplicationMessage"]
old-location: direct3ddxgi\idxgiinfoqueue_addapplicationmessage.htm
tech.root: direct3ddxgi
ms.assetid: 30245BF0-C0AF-4780-A55F-D55A331427FA
ms.date: 12/05/2018
ms.keywords: AddApplicationMessage, AddApplicationMessage method [DXGI], AddApplicationMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],AddApplicationMessage method, IDXGIInfoQueue.AddApplicationMessage, IDXGIInfoQueue::AddApplicationMessage, direct3ddxgi.idxgiinfoqueue_addapplicationmessage, dxgidebug/IDXGIInfoQueue::AddApplicationMessage
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
 - IDXGIInfoQueue::AddApplicationMessage
 - dxgidebug/IDXGIInfoQueue::AddApplicationMessage
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
 - IDXGIInfoQueue.AddApplicationMessage
---

# IDXGIInfoQueue::AddApplicationMessage


## -description

Adds a user-defined message to the message queue and sends that message to the debug output.

## -parameters

### -param Severity [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.

### -param pDescription [in]

The message string.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>