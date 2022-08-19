---
UID: NF:d3d9helper.IDirect3DDevice9.GetDisplayMode
title: IDirect3DDevice9::GetDisplayMode (d3d9helper.h)
description: The IDirect3DDevice9::GetDisplayMode method (d3d9.h) retrieves the display mode's spatial resolution, color resolution, and refresh frequency.
helpviewer_keywords: ["9b212895-5a3c-2630-7af4-0caee7db56cb","GetDisplayMode","GetDisplayMode method [Direct3D 9]","GetDisplayMode method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetDisplayMode method","IDirect3DDevice9.GetDisplayMode","IDirect3DDevice9::GetDisplayMode","d3d9helper/IDirect3DDevice9::GetDisplayMode","direct3d9.idirect3ddevice9__getdisplaymode"]
old-location: direct3d9\idirect3ddevice9__getdisplaymode.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdisplaymode.htm
ms.date: 08/11/2022
ms.keywords: 9b212895-5a3c-2630-7af4-0caee7db56cb, GetDisplayMode, GetDisplayMode method [Direct3D 9], GetDisplayMode method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDisplayMode method, IDirect3DDevice9.GetDisplayMode, IDirect3DDevice9::GetDisplayMode, d3d9helper/IDirect3DDevice9::GetDisplayMode, direct3d9.idirect3ddevice9__getdisplaymode
req.header: d3d9helper.h
req.include-header: D3D9.h
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
 - IDirect3DDevice9::GetDisplayMode
 - d3d9helper/IDirect3DDevice9::GetDisplayMode
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
 - IDirect3DDevice9.GetDisplayMode
---

# IDirect3DDevice9::GetDisplayMode


## -description

Retrieves the display mode's spatial resolution, color resolution, and refresh frequency.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer specifying the swap chain.

### -param pMode [out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymode">D3DDISPLAYMODE</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplaymode">D3DDISPLAYMODE</a> structure containing data about the display mode of the adapter. As opposed to the display mode of the device, which may not be active if the device does not own full-screen mode.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
