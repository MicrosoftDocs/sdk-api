---
UID: NF:d3d9.IDirect3DDevice9Ex.GetMaximumFrameLatency
title: IDirect3DDevice9Ex::GetMaximumFrameLatency (d3d9.h)
description: Retrieves the number of frames of data that the system is allowed to queue.
helpviewer_keywords: ["16bada79-bbf9-2bb3-c2f1-cae31cf742be","GetMaximumFrameLatency","GetMaximumFrameLatency method [Direct3D 9]","GetMaximumFrameLatency method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","GetMaximumFrameLatency method","IDirect3DDevice9Ex.GetMaximumFrameLatency","IDirect3DDevice9Ex::GetMaximumFrameLatency","d3d9/IDirect3DDevice9Ex::GetMaximumFrameLatency","direct3d9.idirect3ddevice9ex_getmaximumframelatency"]
old-location: direct3d9\idirect3ddevice9ex_getmaximumframelatency.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_getmaximumframelatency.htm
ms.date: 12/05/2018
ms.keywords: 16bada79-bbf9-2bb3-c2f1-cae31cf742be, GetMaximumFrameLatency, GetMaximumFrameLatency method [Direct3D 9], GetMaximumFrameLatency method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],GetMaximumFrameLatency method, IDirect3DDevice9Ex.GetMaximumFrameLatency, IDirect3DDevice9Ex::GetMaximumFrameLatency, d3d9/IDirect3DDevice9Ex::GetMaximumFrameLatency, direct3d9.idirect3ddevice9ex_getmaximumframelatency
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9Ex::GetMaximumFrameLatency
 - d3d9/IDirect3DDevice9Ex::GetMaximumFrameLatency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9Ex.GetMaximumFrameLatency
---

# IDirect3DDevice9Ex::GetMaximumFrameLatency


## -description

Retrieves the number of frames of data that the system is allowed to queue.

## -parameters

### -param pMaxLatency [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Returns the number of frames that can be queued for render. The value is typically 3, but can range from 1 to 20.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEREMOVED, D3DERR_DRIVERINTERNALERROR, D3DERR_INVALIDCALL, or D3DERR_OUTOFVIDEOMEMORY (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).

## -remarks

Frame latency is the number of frames that are allowed to be stored in a queue, before submission for rendering. Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.

It is often beneficial for applications that have no user input (for example, video playback) to queue more than 3 frames of data.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>