---
UID: NF:d3d9.IDirect3DDevice9.UpdateSurface
title: IDirect3DDevice9::UpdateSurface (d3d9.h)
description: The IDirect3DDevice9::UpdateSurface method (d3d9.h) copies rectangular subsets of pixels from one surface to another.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","UpdateSurface method","IDirect3DDevice9.UpdateSurface","IDirect3DDevice9::UpdateSurface","UpdateSurface","UpdateSurface method [Direct3D 9]","UpdateSurface method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::UpdateSurface","df5d6a49-ae43-30a0-f148-f2df8e51de81","direct3d9.idirect3ddevice9__updatesurface"]
old-location: direct3d9\idirect3ddevice9__updatesurface.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__updatesurface.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],UpdateSurface method, IDirect3DDevice9.UpdateSurface, IDirect3DDevice9::UpdateSurface, UpdateSurface, UpdateSurface method [Direct3D 9], UpdateSurface method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::UpdateSurface, df5d6a49-ae43-30a0-f148-f2df8e51de81, direct3d9.idirect3ddevice9__updatesurface
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
 - IDirect3DDevice9::UpdateSurface
 - d3d9/IDirect3DDevice9::UpdateSurface
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
 - IDirect3DDevice9.UpdateSurface
---

# IDirect3DDevice9::UpdateSurface


## -description

Copies rectangular subsets of pixels from one surface to another.

## -parameters

### -param pSourceSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the source surface. This parameter must point to a different surface than pDestinationSurface.

### -param pSourceRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a rectangle on the source surface. Specifying <b>NULL</b> for this parameter causes the entire surface to be copied.

### -param pDestinationSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface, representing the destination surface.

### -param pDestPoint [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">POINT</a>*</b>

Pointer to the upper left corner of the destination rectangle. Specifying <b>NULL</b> for this parameter causes the entire surface to be copied.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL.

## -remarks

This method is similar to CopyRects in DirectX 8.

This function has the following restrictions.

<ul>
<li>The source surface must have been created with D3DPOOL_SYSTEMMEM.</li>
<li>The destination surface must have been created with D3DPOOL_DEFAULT.</li>
<li>Neither surface can be locked or holding an outstanding device context.</li>
<li>Neither surface can be created with multisampling. The only valid flag for both surfaces is D3DMULTISAMPLE_NONE.</li>
<li>The surface format cannot be a depth stencil format.</li>
<li>The source and dest rects must fit within the surface.</li>
<li>No stretching or shrinking is allowed (the rects must be the same size).</li>
<li>The source format must match the dest format.</li>
</ul>
The following table shows the supported combinations.

<table>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<td></td>
<td>Texture</td>
<td>RT texture</td>
<td>RT</td>
<td>Off-screen plain</td>
</tr>
<tr>
<th>Src formats</th>
<td>Texture</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes*</td>
<td>Yes</td>
</tr>
<tr>
<th></th>
<td>RT texture</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<td>RT</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<td>Off-screen plain</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>
 

* If the driver does not support the requested copy, it will be emulated using lock and copy.

If the application needs to copy data from a D3DPOOL_DEFAULT render target to a D3DPOOL_SYSTEMMEM surface, it can use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrendertargetdata">GetRenderTargetData</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
