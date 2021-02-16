---
UID: NF:dxgidebug.IDXGIInfoQueue.GetMuteDebugOutput
title: IDXGIInfoQueue::GetMuteDebugOutput (dxgidebug.h)
description: Determines whether the debug output is turned on or off.
helpviewer_keywords: ["GetMuteDebugOutput","GetMuteDebugOutput method [DXGI]","GetMuteDebugOutput method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetMuteDebugOutput method","IDXGIInfoQueue.GetMuteDebugOutput","IDXGIInfoQueue::GetMuteDebugOutput","direct3ddxgi.idxgiinfoqueue_getmutedebugoutput","dxgidebug/IDXGIInfoQueue::GetMuteDebugOutput"]
old-location: direct3ddxgi\idxgiinfoqueue_getmutedebugoutput.htm
tech.root: direct3ddxgi
ms.assetid: 8123DE14-31C1-4304-A295-C7D0C3633C36
ms.date: 12/05/2018
ms.keywords: GetMuteDebugOutput, GetMuteDebugOutput method [DXGI], GetMuteDebugOutput method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetMuteDebugOutput method, IDXGIInfoQueue.GetMuteDebugOutput, IDXGIInfoQueue::GetMuteDebugOutput, direct3ddxgi.idxgiinfoqueue_getmutedebugoutput, dxgidebug/IDXGIInfoQueue::GetMuteDebugOutput
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
 - IDXGIInfoQueue::GetMuteDebugOutput
 - dxgidebug/IDXGIInfoQueue::GetMuteDebugOutput
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
 - IDXGIInfoQueue.GetMuteDebugOutput
---

# IDXGIInfoQueue::GetMuteDebugOutput


## -description

Determines whether the debug output is turned on or off.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the mute status.

## -returns

Returns a Boolean value that specifies whether the debug output is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>