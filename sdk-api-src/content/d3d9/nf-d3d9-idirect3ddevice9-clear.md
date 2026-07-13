---
UID: NF:d3d9.IDirect3DDevice9.Clear
title: IDirect3DDevice9::Clear (d3d9.h)
description: The IDirect3DDevice9::Clear method (d3d9.h) clears one or more surfaces such as a render target, multiple render targets, a stencil buffer, or a depth buffer. 
helpviewer_keywords: ["Clear","Clear method [Direct3D 9]","Clear method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","Clear method","IDirect3DDevice9.Clear","IDirect3DDevice9::Clear","d3d9helper/IDirect3DDevice9::Clear","d8af3d4c-75ea-6282-a8b9-4d9c94a8fbc3","direct3d9.idirect3ddevice9__clear"]
old-location: direct3d9\idirect3ddevice9__clear.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__clear.htm
ms.date: 08/10/2022
ms.keywords: Clear, Clear method [Direct3D 9], Clear method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],Clear method, IDirect3DDevice9.Clear, IDirect3DDevice9::Clear, d3d9helper/IDirect3DDevice9::Clear, d8af3d4c-75ea-6282-a8b9-4d9c94a8fbc3, direct3d9.idirect3ddevice9__clear
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
 - IDirect3DDevice9::Clear
 - d3d9/IDirect3DDevice9::Clear
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
 - IDirect3DDevice9.Clear
---

# IDirect3DDevice9::Clear


## -description

Clears one or more surfaces such as a render target, <a href="/windows/desktop/direct3d9/multiple-render-targets">multiple render targets</a>, a stencil buffer, and a depth buffer.

## -parameters

### -param Count [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Number of rectangles in the array at pRects. Must be set to 0 if pRects is <b>NULL</b>. May not be 0 if pRects is a valid pointer.

### -param pRects [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3drect">D3DRECT</a>*</b>

Pointer to an array of <a href="/windows/desktop/direct3d9/d3drect">D3DRECT</a> structures that describe the rectangles to clear. Set a rectangle to the dimensions of the rendering target to clear the entire surface. Each rectangle uses screen coordinates that correspond to points on the render target. Coordinates are clipped to the bounds of the viewport rectangle. To indicate that the entire viewport rectangle is to be cleared, set this parameter to <b>NULL</b> and Count to 0.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of one or more <a href="/windows/desktop/direct3d9/d3dclear">D3DCLEAR</a> flags that specify the surface(s) that will be cleared.

### -param Color [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcolor">D3DCOLOR</a></b>

Clear a render target to this ARGB color.

### -param Z [in]

Type: <b>float</b>

Clear the depth buffer to this new z value which ranges from 0 to 1. See remarks.

### -param Stencil [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Clear the stencil buffer to this new value which ranges from 0 to 2ⁿ-1 (n is the bit depth of the stencil buffer). See remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.

## -remarks

Use this method to clear a surface including: a render target, all render targets in an MRT, a stencil buffer, or a depth buffer. Flags determines how many surfaces are cleared. Use pRects to clear a subset of a surface defined by an array of rectangles.

<b>IDirect3DDevice9::Clear</b> will fail if you:

<ul>
<li>Try to clear either the depth buffer or the stencil buffer of a render target that does not have an attached depth buffer.</li>
<li>Try to clear the stencil buffer when the depth buffer does not contain stencil data.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
