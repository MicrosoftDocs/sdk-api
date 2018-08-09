---
UID: NF:d3d9.IDirect3DDevice9Ex.ComposeRects
title: IDirect3DDevice9Ex::ComposeRects
author: windows-sdk-content
description: Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.
old-location: direct3d9\idirect3ddevice9ex_composerect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_composerect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 097e4733-c996-6415-2d0b-16df84b70922, ComposeRects, ComposeRects method [Direct3D 9], ComposeRects method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],ComposeRects method, IDirect3DDevice9Ex.ComposeRects, IDirect3DDevice9Ex::ComposeRects, d3d9/IDirect3DDevice9Ex::ComposeRects, direct3d9.idirect3ddevice9ex_composerect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9Ex::ComposeRects


## -description


Copy a text string to one surface using an alphabet of glyphs on another surface. Composition is done by the GPU using bitwise operations.


## -parameters




### -param pSrc




### -param pDst




### -param pSrcRectDescs




### -param NumRects [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rectangles or glyphs that are used in the operation. The number applies to both the source and destination surfaces. The range is 0 to <a href="https://msdn.microsoft.com/en-us/library/Bb509547(v=VS.85).aspx">D3DCOMPOSERECTS_MAXNUMRECTS</a>.


### -param pDstRectDescs




### -param Operation [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb509546(v=VS.85).aspx">D3DCOMPOSERECTSOP</a></b>

Specifies how to combine the source and destination surfaces. See <a href="https://msdn.microsoft.com/en-us/library/Bb509546(v=VS.85).aspx">D3DCOMPOSERECTSOP</a>.


### -param Xoffset




### -param Yoffset






#### - pSource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>*</b>

A pointer to a source surface (prepared by <a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>) that supplies the alphabet glyphs. This surface must be created with the <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE_TEXTAPI</a> flag.


#### - pDestination [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>*</b>

A pointer to the destination surface (prepared by <a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>) that receives the glyph data. The surface must be part of a texture.


#### - pSrcRectDescriptors [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205915(v=VS.85).aspx">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="https://msdn.microsoft.com/en-us/library/Bb205915(v=VS.85).aspx">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="https://msdn.microsoft.com/en-us/library/Bb509544(v=VS.85).aspx">D3DCOMPOSERECTDESC</a>) that enclose the desired glyphs in the source surface.


#### - pDstRectDescriptors [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205915(v=VS.85).aspx">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="https://msdn.microsoft.com/en-us/library/Bb205915(v=VS.85).aspx">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="https://msdn.microsoft.com/en-us/library/Bb509545(v=VS.85).aspx">D3DCOMPOSERECTDESTINATION</a>) that describe the destination to which the indicated glyph from the source surface will be copied.


#### - XOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to the <i>x</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.


#### - YOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to the <i>y</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.




## -remarks



Glyphs from a one-bit source surface are put together into another one-bit texture surface with this method. The destination surface can then be used as the source for a normal texturing operation that will filter and scale the strings of text onto some other non-monochrome surface.

This method has several constraints (which are similar to <a href="https://msdn.microsoft.com/en-us/library/Bb174471(v=VS.85).aspx">StretchRect</a>):

<ul>
<li>Surfaces cannot be locked.</li>
<li>The source and destination surfaces cannot be the same surface.</li>
<li>The source and destination surfaces must be created with the <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFMT_A1</a> format.</li>
<li>The source surface and both vertex buffers must be created with the <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL_DEFAULT</a> flag.</li>
<li>The destination surface must be created with either the <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL_DEFAULT</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL_SYSTEMMEM</a> flags.</li>
<li>The source rectangles must be within the source surface.</li>
</ul>
The method is not recorded in state blocks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

