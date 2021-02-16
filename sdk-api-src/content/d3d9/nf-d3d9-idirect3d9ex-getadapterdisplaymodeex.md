---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterDisplayModeEx
title: IDirect3D9Ex::GetAdapterDisplayModeEx (d3d9.h)
description: Retrieves the current display mode and rotation settings of the adapter.
helpviewer_keywords: ["GetAdapterDisplayModeEx","GetAdapterDisplayModeEx method [Direct3D 9]","GetAdapterDisplayModeEx method [Direct3D 9]","IDirect3D9Ex interface","IDirect3D9Ex interface [Direct3D 9]","GetAdapterDisplayModeEx method","IDirect3D9Ex.GetAdapterDisplayModeEx","IDirect3D9Ex::GetAdapterDisplayModeEx","a9a9a87a-36fb-8647-d001-d83d9020a82e","d3d9/IDirect3D9Ex::GetAdapterDisplayModeEx","direct3d9.idirect3d9ex_getadapterdisplaymodeex"]
old-location: direct3d9\idirect3d9ex_getadapterdisplaymodeex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadapterdisplaymodeex.htm
ms.date: 12/05/2018
ms.keywords: GetAdapterDisplayModeEx, GetAdapterDisplayModeEx method [Direct3D 9], GetAdapterDisplayModeEx method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],GetAdapterDisplayModeEx method, IDirect3D9Ex.GetAdapterDisplayModeEx, IDirect3D9Ex::GetAdapterDisplayModeEx, a9a9a87a-36fb-8647-d001-d83d9020a82e, d3d9/IDirect3D9Ex::GetAdapterDisplayModeEx, direct3d9.idirect3d9ex_getadapterdisplaymodeex
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
 - IDirect3D9Ex::GetAdapterDisplayModeEx
 - d3d9/IDirect3D9Ex::GetAdapterDisplayModeEx
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
 - IDirect3D9Ex.GetAdapterDisplayModeEx
---

# IDirect3D9Ex::GetAdapterDisplayModeEx


## -description

Retrieves the current display mode and rotation settings of the adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number that denotes the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter.

### -param pMode [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. Can be set to <b>NULL</b>.

### -param pRotation [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplayrotation">D3DDISPLAYROTATION</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplayrotation">D3DDISPLAYROTATION</a> structure indicating the type of screen rotation the application will do. The value returned through this pointer is important when the <a href="/windows/desktop/direct3d9/d3dpresentflag">D3DPRESENTFLAG_NOAUTOROTATE</a> flag is used; otherwise, it can be set to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. 



If <i>Adapter</i> is out of range or <i>pMode</i> is invalid, this method returns D3DERR_INVALIDCALL.

## -remarks

<b>GetAdapterDisplayModeEx</b> does not return the correct format when the display is in an extended format, such as 2:10:10:10. Instead, it returns the format X8R8G8B8.

To windowed applications, a value of S_PRESENT_MODE_CHANGED returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex">PresentEx</a> or <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">CheckDeviceState</a> indicates that the display mode changed and that the current display mode might have a different format. To avoid a color-converting Present blt, windowed applications can optionally get new display mode information by using this method and adjusting its swap chain format accordingly. This method returns D3DERR_NOTAVAILABLE if this head is no longer part of the desktop or if the monitor is disconnected.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>