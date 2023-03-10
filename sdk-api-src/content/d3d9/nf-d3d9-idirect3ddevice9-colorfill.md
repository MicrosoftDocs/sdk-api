---
UID: NF:d3d9.IDirect3DDevice9.ColorFill
title: IDirect3DDevice9::ColorFill (d3d9.h)
description: The IDirect3DDevice9::ColorFill method (d3d9.h) allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color.
helpviewer_keywords: ["ColorFill","ColorFill method [Direct3D 9]","ColorFill method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","ColorFill method","IDirect3DDevice9.ColorFill","IDirect3DDevice9::ColorFill","b637fa24-0e80-8d43-dece-17fb81ac14e4","d3d9helper/IDirect3DDevice9::ColorFill","direct3d9.idirect3ddevice9__colorfill"]
old-location: direct3d9\idirect3ddevice9__colorfill.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__colorfill.htm
ms.date: 08/10/2022
ms.keywords: ColorFill, ColorFill method [Direct3D 9], ColorFill method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],ColorFill method, IDirect3DDevice9.ColorFill, IDirect3DDevice9::ColorFill, b637fa24-0e80-8d43-dece-17fb81ac14e4, d3d9helper/IDirect3DDevice9::ColorFill, direct3d9.idirect3ddevice9__colorfill
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
 - IDirect3DDevice9::ColorFill
 - d3d9/IDirect3DDevice9::ColorFill
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
 - IDirect3DDevice9.ColorFill
---

# IDirect3DDevice9::ColorFill


## -description

Allows an application to fill a rectangular area of a D3DPOOL_DEFAULT surface with a specified color.

## -parameters

### -param pSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to the surface to be filled.

### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the source rectangle. Using <b>NULL</b> means that the entire surface will be filled.

### -param color [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcolor">D3DCOLOR</a></b>

Color used for filling.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.

## -remarks

This method can only be applied to a render target, a render-target texture surface, or an off-screen plain surface with a pool type of D3DPOOL_DEFAULT.

<b>IDirect3DDevice9::ColorFill</b> will work with all formats. However, when using a reference or software device, the only formats supported are D3DFMT_X1R5G5B5, D3DFMT_A1R5G5B5, D3DFMT_R5G6B5, D3DFMT_X8R8G8B8, D3DFMT_A8R8G8B8, D3DFMT_YUY2, D3DFMT_G8R8_G8B8, D3DFMT_UYVY, D3DFMT_R8G8_B8G8, D3DFMT_R16F, D3DFMT_G16R16F, D3DFMT_A16B16G16R16F, D3DFMT_R32F, D3DFMT_G32R32F, and D3DFMT_A32B32G32R32F.

When using a DirectX 7 or DirectX 8.x driver, the only YUV formats supported are D3DFMT_UYVY and D3DFMT_YUY2.

## -see-also

<a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
