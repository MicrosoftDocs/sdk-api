---
UID: NF:d3d9.IDirect3DDevice9Ex.GetDisplayModeEx
title: IDirect3DDevice9Ex::GetDisplayModeEx (d3d9.h)
description: Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings. (IDirect3DDevice9Ex.GetDisplayModeEx)
helpviewer_keywords: ["3de20b27-6ffa-11bb-e9a5-d1af96f798ac","GetDisplayModeEx","GetDisplayModeEx method [Direct3D 9]","GetDisplayModeEx method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","GetDisplayModeEx method","IDirect3DDevice9Ex.GetDisplayModeEx","IDirect3DDevice9Ex::GetDisplayModeEx","d3d9/IDirect3DDevice9Ex::GetDisplayModeEx","direct3d9.idirect3ddevice9ex_getdisplaymodeex"]
old-location: direct3d9\idirect3ddevice9ex_getdisplaymodeex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_getdisplaymodeex.htm
ms.date: 12/05/2018
ms.keywords: 3de20b27-6ffa-11bb-e9a5-d1af96f798ac, GetDisplayModeEx, GetDisplayModeEx method [Direct3D 9], GetDisplayModeEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],GetDisplayModeEx method, IDirect3DDevice9Ex.GetDisplayModeEx, IDirect3DDevice9Ex::GetDisplayModeEx, d3d9/IDirect3DDevice9Ex::GetDisplayModeEx, direct3d9.idirect3ddevice9ex_getdisplaymodeex
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
 - IDirect3DDevice9Ex::GetDisplayModeEx
 - d3d9/IDirect3DDevice9Ex::GetDisplayModeEx
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
 - IDirect3DDevice9Ex.GetDisplayModeEx
---

# IDirect3DDevice9Ex::GetDisplayModeEx


## -description

Retrieves the display mode's spatial resolution, color resolution, refresh frequency, and rotation settings.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer specifying the swap chain.

### -param pMode [out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode. Can be set to <b>NULL</b>.

### -param pRotation [out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplayrotation">D3DDISPLAYROTATION</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplayrotation">D3DDISPLAYROTATION</a> indicating the type of screen rotation the application will do. The value returned through this pointer is important when the <a href="/windows/desktop/direct3d9/d3dpresentflag">D3DPRESENTFLAG_NOAUTOROTATE</a> flag is used; otherwise, it can be set to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>
