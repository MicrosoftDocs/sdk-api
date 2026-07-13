---
UID: NF:dxgi.IDXGIDevice.SetGPUThreadPriority
title: IDXGIDevice::SetGPUThreadPriority (dxgi.h)
description: Sets the GPU thread priority.
helpviewer_keywords: ["IDXGIDevice interface [DXGI]","SetGPUThreadPriority method","IDXGIDevice.SetGPUThreadPriority","IDXGIDevice::SetGPUThreadPriority","SetGPUThreadPriority","SetGPUThreadPriority method [DXGI]","SetGPUThreadPriority method [DXGI]","IDXGIDevice interface","b610ce23-f003-9031-4c67-b5013c5af229","direct3ddxgi.idxgidevice_setgputhreadpriority","dxgi/IDXGIDevice::SetGPUThreadPriority"]
old-location: direct3ddxgi\idxgidevice_setgputhreadpriority.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_setgputhreadpriority.htm
ms.date: 12/05/2018
ms.keywords: IDXGIDevice interface [DXGI],SetGPUThreadPriority method, IDXGIDevice.SetGPUThreadPriority, IDXGIDevice::SetGPUThreadPriority, SetGPUThreadPriority, SetGPUThreadPriority method [DXGI], SetGPUThreadPriority method [DXGI],IDXGIDevice interface, b610ce23-f003-9031-4c67-b5013c5af229, direct3ddxgi.idxgidevice_setgputhreadpriority, dxgi/IDXGIDevice::SetGPUThreadPriority
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice::SetGPUThreadPriority
 - dxgi/IDXGIDevice::SetGPUThreadPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice.SetGPUThreadPriority
---

# IDXGIDevice::SetGPUThreadPriority


## -description

Sets the GPU thread priority.

## -parameters

### -param Priority

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value that specifies the required GPU thread priority. See the [Remarks](#remarks) section in this topic.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Return S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Priority</i> parameter is invalid.

## -remarks

To use the <b>SetGPUThreadPriority</b> method, you should have a comprehensive understanding of GPU scheduling. If used inappropriately, the <b>SetGPUThreadPriority</b> method can impede rendering speed and result in a poor user experience, so profile your application to understand impact of priority change on application and on system.

The values for the <i>Priority</i> parameter function as follows:
<b>Priority Values Bit Definition:</b>
<ul>
Bit 0-4  : Priority Value <br>
Bit 5-29 : Reserved <br>
Bit 30   : Absolute Priority Flag ( D3DKMT_SETCONTEXTSCHEDULINGPRIORITY_ABSOLUTE ), can be ORed with Priority Value Bits [4:0] (Only valid for Windows 10+, else not used)<br>
Bit 31   : Signed bit <br>
</ul>

Bit 30 (Absolute Priority Flag) can be used to control the mode of operation for this API. 

<b>Relative Priority Mode</b> : API will use this mode when bit 30 value is set to 0. In this mode, <b>Priority</b> value must be between -7 and 7, inclusive, where priority value 0 represents normal priority (Default for all contexts) and -7 represents Idle priority. Bit 31 is used to control sign of the priority.

<b>Absolute Priority Mode</b> : API will use this mode when bit 30 value is set to 1. In this mode, <b>Priority</b> value (for bits[4:0]) must be between 0 and 31. Meaning of these priority levels is described below. Use D3DKMT_SETCONTEXTSCHEDULINGPRIORITY_ABSOLUTE only if you have thorough understanding of dxgkrnl/graphics priorities and understand repercussions of changing them.

<b>Priority Values Bits[4:0]</b> translates to following priority values:
<ul>
0     : Idle Priority   - Forward progress is not guaranteed if higher priorties use most of the accelerator time.<br>
1     : Normal Priority - Most of the processes use this priority with forward progress guarantee.<br>
2 -15 : Reserved        - <br>
16-29 : Soft Realtime   - Preempts lower priorities and periodically yields to lower priorities to ensure their forward progress.<br>
30    : Hard Realtime   - Used for extremely latency sensitive well bounded workloads. This priority does not yield to lower priorities. <br>
31    : Internal Use <br>
</ul>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getgputhreadpriority">IDXGIDevice::GetGPUThreadPriority</a>
