---
UID: NF:dxgidebug.IDXGIInfoQueue.SetBreakOnSeverity
title: IDXGIInfoQueue::SetBreakOnSeverity (dxgidebug.h)
description: Sets a message severity level to break on when a message with that severity level passes through the storage filter.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","SetBreakOnSeverity method","IDXGIInfoQueue.SetBreakOnSeverity","IDXGIInfoQueue::SetBreakOnSeverity","SetBreakOnSeverity","SetBreakOnSeverity method [DXGI]","SetBreakOnSeverity method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_setbreakonseverity","dxgidebug/IDXGIInfoQueue::SetBreakOnSeverity"]
old-location: direct3ddxgi\idxgiinfoqueue_setbreakonseverity.htm
tech.root: direct3ddxgi
ms.assetid: 3316A9E5-F65B-4162-9A5E-CDB5CD65FBF8
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetBreakOnSeverity method, IDXGIInfoQueue.SetBreakOnSeverity, IDXGIInfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [DXGI], SetBreakOnSeverity method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setbreakonseverity, dxgidebug/IDXGIInfoQueue::SetBreakOnSeverity
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
 - IDXGIInfoQueue::SetBreakOnSeverity
 - dxgidebug/IDXGIInfoQueue::SetBreakOnSeverity
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
 - IDXGIInfoQueue.SetBreakOnSeverity
---

# IDXGIInfoQueue::SetBreakOnSeverity


## -description

Sets a message severity level to break on when a message with that severity level passes through the storage filter.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that sets the breaking condition.

### -param Severity [in]

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_info_queue_message_severity">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.

### -param bEnable [in]

A Boolean value that specifies whether <b>SetBreakOnSeverity</b> turns on or off this breaking condition (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>