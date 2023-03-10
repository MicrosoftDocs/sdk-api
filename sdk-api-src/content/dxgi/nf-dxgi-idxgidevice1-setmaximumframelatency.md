---
UID: NF:dxgi.IDXGIDevice1.SetMaximumFrameLatency
title: IDXGIDevice1::SetMaximumFrameLatency (dxgi.h)
description: Sets the number of frames that the system is allowed to queue for rendering.
helpviewer_keywords: ["IDXGIDevice1 interface [DXGI]","SetMaximumFrameLatency method","IDXGIDevice1.SetMaximumFrameLatency","IDXGIDevice1::SetMaximumFrameLatency","SetMaximumFrameLatency","SetMaximumFrameLatency method [DXGI]","SetMaximumFrameLatency method [DXGI]","IDXGIDevice1 interface","da92b152-07cc-06ca-caa5-a8982fe8fc2f","direct3ddxgi.idxgidevice1_setmaximumframelatency","dxgi/IDXGIDevice1::SetMaximumFrameLatency"]
old-location: direct3ddxgi\idxgidevice1_setmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: ea477f33-2dba-44ac-9b47-8fd2ce6cec30
ms.date: 12/05/2018
ms.keywords: IDXGIDevice1 interface [DXGI],SetMaximumFrameLatency method, IDXGIDevice1.SetMaximumFrameLatency, IDXGIDevice1::SetMaximumFrameLatency, SetMaximumFrameLatency, SetMaximumFrameLatency method [DXGI], SetMaximumFrameLatency method [DXGI],IDXGIDevice1 interface, da92b152-07cc-06ca-caa5-a8982fe8fc2f, direct3ddxgi.idxgidevice1_setmaximumframelatency, dxgi/IDXGIDevice1::SetMaximumFrameLatency
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIDevice1::SetMaximumFrameLatency
 - dxgi/IDXGIDevice1::SetMaximumFrameLatency
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
 - IDXGIDevice1.SetMaximumFrameLatency
---

# IDXGIDevice1::SetMaximumFrameLatency


## -description

Sets the number of frames that the system is allowed to queue for rendering.

## -parameters

### -param MaxLatency

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The maximum number of back buffer frames that a driver can queue. The value defaults to 3, but 
      can range from 1 to 16. A value of 0 will reset latency to the default.  For multi-head devices, this value is specified per-head.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, DXGI_ERROR_DEVICE_REMOVED if the device was removed.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

Frame latency is the number of frames that are allowed to be stored in a queue before submission for rendering.  Latency is often used to 
    control how the CPU chooses between responding to user input and frames that are in the render queue.  It is often beneficial for applications that 
    have no user input (for example, video playback) to queue more than 3 frames of data.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency">IDXGIDevice1::GetMaximumFrameLatency</a>