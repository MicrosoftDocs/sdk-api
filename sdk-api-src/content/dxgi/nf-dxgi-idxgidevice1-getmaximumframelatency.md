---
UID: NF:dxgi.IDXGIDevice1.GetMaximumFrameLatency
title: IDXGIDevice1::GetMaximumFrameLatency (dxgi.h)
description: Gets the number of frames that the system is allowed to queue for rendering.
helpviewer_keywords: ["65e01dd1-b488-81d7-8806-77a7e4bb8f02","GetMaximumFrameLatency","GetMaximumFrameLatency method [DXGI]","GetMaximumFrameLatency method [DXGI]","IDXGIDevice1 interface","IDXGIDevice1 interface [DXGI]","GetMaximumFrameLatency method","IDXGIDevice1.GetMaximumFrameLatency","IDXGIDevice1::GetMaximumFrameLatency","direct3ddxgi.idxgidevice1_getmaximumframelatency","dxgi/IDXGIDevice1::GetMaximumFrameLatency"]
old-location: direct3ddxgi\idxgidevice1_getmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: 87b98c47-3556-4588-97b2-c935d7052286
ms.date: 12/05/2018
ms.keywords: 65e01dd1-b488-81d7-8806-77a7e4bb8f02, GetMaximumFrameLatency, GetMaximumFrameLatency method [DXGI], GetMaximumFrameLatency method [DXGI],IDXGIDevice1 interface, IDXGIDevice1 interface [DXGI],GetMaximumFrameLatency method, IDXGIDevice1.GetMaximumFrameLatency, IDXGIDevice1::GetMaximumFrameLatency, direct3ddxgi.idxgidevice1_getmaximumframelatency, dxgi/IDXGIDevice1::GetMaximumFrameLatency
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
 - IDXGIDevice1::GetMaximumFrameLatency
 - dxgi/IDXGIDevice1::GetMaximumFrameLatency
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
 - IDXGIDevice1.GetMaximumFrameLatency
---

# IDXGIDevice1::GetMaximumFrameLatency


## -description

Gets the number of frames that the system is allowed to queue for rendering.

## -parameters

### -param pMaxLatency [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

This value is set to the number of frames that can be queued for render.  
      This value defaults to 3, but can range from 1 to 16.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following members of the <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a> enumerated type:

<ul>
<li><b>D3DERR_DEVICELOST</b></li>
<li><b>D3DERR_DEVICEREMOVED</b></li>
<li><b>D3DERR_DRIVERINTERNALERROR</b></li>
<li><b>D3DERR_INVALIDCALL</b></li>
<li><b>D3DERR_OUTOFVIDEOMEMORY</b></li>
</ul>

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

Frame latency is the number of frames that are allowed to be stored in a queue before submission for rendering.  Latency is often 
    used to control how the CPU chooses between responding to user input and frames that are in the render queue.  It is often beneficial for applications 
    that have no user input (for example, video playback) to queue more than 3 frames of data.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency">IDXGIDevice1::SetMaximumFrameLatency</a>