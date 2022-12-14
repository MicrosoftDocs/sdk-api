---
UID: NF:d3d9.IDirect3DDevice9.GetRasterStatus
title: IDirect3DDevice9::GetRasterStatus (d3d9.h)
description: The IDirect3DDevice9::GetRasterStatus method (d3d9.h) returns information describing the raster of the monitor on which the swap chain is presented.
helpviewer_keywords: ["GetRasterStatus","GetRasterStatus method [Direct3D 9]","GetRasterStatus method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetRasterStatus method","IDirect3DDevice9.GetRasterStatus","IDirect3DDevice9::GetRasterStatus","a1fc6bf1-1e43-8a94-f293-1f38f3147f02","d3d9helper/IDirect3DDevice9::GetRasterStatus","direct3d9.idirect3ddevice9__getrasterstatus"]
old-location: direct3d9\idirect3ddevice9__getrasterstatus.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getrasterstatus.htm
ms.date: 08/10/2022
ms.keywords: GetRasterStatus, GetRasterStatus method [Direct3D 9], GetRasterStatus method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetRasterStatus method, IDirect3DDevice9.GetRasterStatus, IDirect3DDevice9::GetRasterStatus, a1fc6bf1-1e43-8a94-f293-1f38f3147f02, d3d9helper/IDirect3DDevice9::GetRasterStatus, direct3d9.idirect3ddevice9__getrasterstatus
req.header: d3d9.h
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
 - IDirect3DDevice9::GetRasterStatus
 - d3d9/IDirect3DDevice9::GetRasterStatus
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
 - IDirect3DDevice9.GetRasterStatus
---

# IDirect3DDevice9::GetRasterStatus


## -description

Returns information describing the raster of the monitor on which the swap chain is presented.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer specifying the swap chain.

### -param pRasterStatus [out]

Type: <b><a href="/windows/desktop/direct3d9/d3draster-status">D3DRASTER_STATUS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3draster-status">D3DRASTER_STATUS</a> structure filled with information about the position or other status of the raster on the monitor driven by this adapter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if pRasterStatus is invalid or if the device does not support reading the current scan line. To determine if the device supports reading the scan line, check for the D3DCAPS_READ_SCANLINE flag in the Caps member of <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>.

## -see-also

<a href="/windows/desktop/direct3d9/d3draster-status">D3DRASTER_STATUS</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
