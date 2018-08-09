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

The number of rectangles or glyphs that are used in the operation. The number applies to both the source and destination surfaces. The range is 0 to <a href="https://msdn.microsoft.com/baf38e21-96b9-496f-8bec-7d2e28c1676d">D3DCOMPOSERECTS_MAXNUMRECTS</a>.


### -param pDstRectDescs




### -param Operation [in]

Type: <b><a href="https://msdn.microsoft.com/4b0e6e48-48e0-4955-bb20-f953fdce785c">D3DCOMPOSERECTSOP</a></b>

Specifies how to combine the source and destination surfaces. See <a href="https://msdn.microsoft.com/4b0e6e48-48e0-4955-bb20-f953fdce785c">D3DCOMPOSERECTSOP</a>.


### -param Xoffset




### -param Yoffset






#### - pSource [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

A pointer to a source surface (prepared by <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>) that supplies the alphabet glyphs. This surface must be created with the <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_TEXTAPI</a> flag.


#### - pDestination [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

A pointer to the destination surface (prepared by <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>) that receives the glyph data. The surface must be part of a texture.


#### - pSrcRectDescriptors [in]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="https://msdn.microsoft.com/ce5d492f-38d1-4e7b-a9c2-68c791c84d0c">D3DCOMPOSERECTDESC</a>) that enclose the desired glyphs in the source surface.


#### - pDstRectDescriptors [in]

Type: <b><a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>*</b>

A pointer to a vertex buffer (see <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>) containing rectangles (see <a href="https://msdn.microsoft.com/eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1">D3DCOMPOSERECTDESTINATION</a>) that describe the destination to which the indicated glyph from the source surface will be copied.


#### - XOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to the <i>x</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.


#### - YOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to the <i>y</i> coordinates of all destination rectangles. This value can be negative, which may cause the glyph to be rejected or clipped if the result is beyond the bounds of the surface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.




## -remarks



Glyphs from a one-bit source surface are put together into another one-bit texture surface with this method. The destination surface can then be used as the source for a normal texturing operation that will filter and scale the strings of text onto some other non-monochrome surface.

This method has several constraints (which are similar to <a href="https://msdn.microsoft.com/1ad6d48f-8420-461a-96b5-e730ac06c393">StretchRect</a>):

<ul>
<li>Surfaces cannot be locked.</li>
<li>The source and destination surfaces cannot be the same surface.</li>
<li>The source and destination surfaces must be created with the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_A1</a> format.</li>
<li>The source surface and both vertex buffers must be created with the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL_DEFAULT</a> flag.</li>
<li>The destination surface must be created with either the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL_DEFAULT</a> or <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL_SYSTEMMEM</a> flags.</li>
<li>The source rectangles must be within the source surface.</li>
</ul>
The method is not recorded in state blocks.




## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

