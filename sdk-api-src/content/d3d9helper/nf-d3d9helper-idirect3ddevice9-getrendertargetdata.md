---
UID: NF:d3d9helper.IDirect3DDevice9.GetRenderTargetData
title: IDirect3DDevice9::GetRenderTargetData (d3d9helper.h)
description: The IDirect3DDevice9::GetRenderTargetData method (d3d9.h) copies the render-target data from device memory to system memory.
helpviewer_keywords: ["GetRenderTargetData","GetRenderTargetData method [Direct3D 9]","GetRenderTargetData method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetRenderTargetData method","IDirect3DDevice9.GetRenderTargetData","IDirect3DDevice9::GetRenderTargetData","d3d9helper/IDirect3DDevice9::GetRenderTargetData","direct3d9.idirect3ddevice9__getrendertargetdata","ef2b445f-f837-5faa-3c68-645f07e7e87b"]
old-location: direct3d9\idirect3ddevice9__getrendertargetdata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getrendertargetdata.htm
ms.date: 08/11/2022
ms.keywords: GetRenderTargetData, GetRenderTargetData method [Direct3D 9], GetRenderTargetData method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetRenderTargetData method, IDirect3DDevice9.GetRenderTargetData, IDirect3DDevice9::GetRenderTargetData, d3d9helper/IDirect3DDevice9::GetRenderTargetData, direct3d9.idirect3ddevice9__getrendertargetdata, ef2b445f-f837-5faa-3c68-645f07e7e87b
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
 - IDirect3DDevice9::GetRenderTargetData
 - d3d9helper/IDirect3DDevice9::GetRenderTargetData
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
 - IDirect3DDevice9.GetRenderTargetData
---

# IDirect3DDevice9::GetRenderTargetData


## -description

Copies the render-target data from device memory to system memory.

## -parameters

### -param pRenderTarget [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> object, representing a render target.

### -param pDestSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> object, representing a destination surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DRIVERINTERNALERROR, D3DERR_DEVICELOST, D3DERR_INVALIDCALL.

## -remarks

The destination surface must be either an off-screen plain surface or a level of a texture (mipmap or cube texture) created with D3DPOOL_SYSTEMMEM.

The source surface must be a regular render target or a level of a render-target texture (mipmap or cube texture) created with POOL_DEFAULT.

This method will fail if:

<ul>
<li>The render target is multisampled.</li>
<li>The source render target is a different size than the destination surface.</li>
<li>The source render target and destination surface formats do not match.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
