---
UID: NF:d3d9.IDirect3DDevice9Ex.ComposeRects
title: IDirect3DDevice9Ex::ComposeRects (d3d9.h)
description: Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.
helpviewer_keywords: ["097e4733-c996-6415-2d0b-16df84b70922","ComposeRects","ComposeRects method [Direct3D 9]","ComposeRects method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","ComposeRects method","IDirect3DDevice9Ex.ComposeRects","IDirect3DDevice9Ex::ComposeRects","d3d9/IDirect3DDevice9Ex::ComposeRects","direct3d9.idirect3ddevice9ex_composerect"]
old-location: direct3d9\idirect3ddevice9ex_composerect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_composerect.htm
ms.date: 12/05/2018
ms.keywords: 097e4733-c996-6415-2d0b-16df84b70922, ComposeRects, ComposeRects method [Direct3D 9], ComposeRects method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],ComposeRects method, IDirect3DDevice9Ex.ComposeRects, IDirect3DDevice9Ex::ComposeRects, d3d9/IDirect3DDevice9Ex::ComposeRects, direct3d9.idirect3ddevice9ex_composerect
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
 - IDirect3DDevice9Ex::ComposeRects
 - d3d9/IDirect3DDevice9Ex::ComposeRects
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
 - IDirect3DDevice9Ex.ComposeRects
---

# IDirect3DDevice9Ex::ComposeRects


## -description

Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.

## -parameters

### -param pSrc [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

A pointer to a source surface (prepared by <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>) that supplies the alphabet glyphs. This surface must be created with the <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_TEXTAPI</a> flag.

### -param pDst [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

A pointer to the destination surface (prepared by <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>) that receives the glyph data. The surface must be part of a texture.

### -param pSrcRectDescs [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="/windows/desktop/direct3d9/d3dcomposerectdesc">D3DCOMPOSERECTDESC</a>) that enclose the desired glyphs in the source surface.

### -param NumRects [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of rectangles or glyphs that are used in the operation. The number applies to both the source and destination surfaces. The range is 0 to <a href="/windows/desktop/direct3d9/d3dcomposerects-maxnumrects">D3DCOMPOSERECTS_MAXNUMRECTS</a>.

### -param pDstRectDescs [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="/windows/desktop/direct3d9/d3dcomposerectdestination">D3DCOMPOSERECTDESTINATION</a>) that describe the destination to which the indicated glyph from the source surface will be copied.

### -param Operation [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dcomposerectsop">D3DCOMPOSERECTSOP</a></b>

Specifies how to combine the source and destination surfaces. See <a href="/windows/desktop/direct3d9/d3dcomposerectsop">D3DCOMPOSERECTSOP</a>.

### -param Xoffset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value added to the <i>x</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.

### -param Yoffset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value added to the <i>y</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.

## -remarks

Glyphs from a one-bit source surface are put together into another one-bit texture surface with this method. The destination surface can then be used as the source for a normal texturing operation that will filter and scale the strings of text onto some other non-monochrome surface.

This method has several constraints (which are similar to <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect">StretchRect</a>):

<ul>
<li>Surfaces cannot be locked.</li>
<li>The source and destination surfaces cannot be the same surface.</li>
<li>The source and destination surfaces must be created with the <a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_A1</a> format.</li>
<li>The source surface and both vertex buffers must be created with the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL_DEFAULT</a> flag.</li>
<li>The destination surface must be created with either the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL_DEFAULT</a> or <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL_SYSTEMMEM</a> flags.</li>
<li>The source rectangles must be within the source surface.</li>
</ul>
The method is not recorded in state blocks.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>