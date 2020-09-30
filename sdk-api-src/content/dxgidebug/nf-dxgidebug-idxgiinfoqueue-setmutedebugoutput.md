---
UID: NF:dxgidebug.IDXGIInfoQueue.SetMuteDebugOutput
title: IDXGIInfoQueue::SetMuteDebugOutput (dxgidebug.h)
description: Turns the debug output on or off.
helpviewer_keywords: ["IDXGIInfoQueue interface [DXGI]","SetMuteDebugOutput method","IDXGIInfoQueue.SetMuteDebugOutput","IDXGIInfoQueue::SetMuteDebugOutput","SetMuteDebugOutput","SetMuteDebugOutput method [DXGI]","SetMuteDebugOutput method [DXGI]","IDXGIInfoQueue interface","direct3ddxgi.idxgiinfoqueue_setmutedebugoutput","dxgidebug/IDXGIInfoQueue::SetMuteDebugOutput"]
old-location: direct3ddxgi\idxgiinfoqueue_setmutedebugoutput.htm
tech.root: direct3ddxgi
ms.assetid: F01E8BCC-CF82-4008-9829-C7EE4AD2973C
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetMuteDebugOutput method, IDXGIInfoQueue.SetMuteDebugOutput, IDXGIInfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method [DXGI], SetMuteDebugOutput method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setmutedebugoutput, dxgidebug/IDXGIInfoQueue::SetMuteDebugOutput
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
 - IDXGIInfoQueue::SetMuteDebugOutput
 - dxgidebug/IDXGIInfoQueue::SetMuteDebugOutput
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
 - IDXGIInfoQueue.SetMuteDebugOutput
---

# IDXGIInfoQueue::SetMuteDebugOutput


## -description

Turns the debug output on or off.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the mute status.

### -param bMute [in]

A Boolean value that specifies whether to turn the debug output on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>