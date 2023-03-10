---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnSeverity
title: IDXGIInfoQueue::GetBreakOnSeverity (dxgidebug.h)
description: Determines whether the break on a message severity level is turned on or off.
helpviewer_keywords: ["GetBreakOnSeverity","GetBreakOnSeverity method [DXGI]","GetBreakOnSeverity method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetBreakOnSeverity method","IDXGIInfoQueue.GetBreakOnSeverity","IDXGIInfoQueue::GetBreakOnSeverity","direct3ddxgi.idxgiinfoqueue_getbreakonseverity","dxgidebug/IDXGIInfoQueue::GetBreakOnSeverity"]
old-location: direct3ddxgi\idxgiinfoqueue_getbreakonseverity.htm
tech.root: direct3ddxgi
ms.assetid: 0E03ABE8-02BC-4721-B92C-87DA5D52D0AD
ms.date: 12/05/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method [DXGI], GetBreakOnSeverity method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnSeverity method, IDXGIInfoQueue.GetBreakOnSeverity, IDXGIInfoQueue::GetBreakOnSeverity, direct3ddxgi.idxgiinfoqueue_getbreakonseverity, dxgidebug/IDXGIInfoQueue::GetBreakOnSeverity
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
 - IDXGIInfoQueue::GetBreakOnSeverity
 - dxgidebug/IDXGIInfoQueue::GetBreakOnSeverity
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
 - IDXGIInfoQueue.GetBreakOnSeverity
---

# IDXGIInfoQueue::GetBreakOnSeverity


## -description

Determines whether the break on a message severity level is turned on or off.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.

### -param Severity [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.

## -returns

Returns a Boolean value that specifies whether this severity of breaking condition is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>