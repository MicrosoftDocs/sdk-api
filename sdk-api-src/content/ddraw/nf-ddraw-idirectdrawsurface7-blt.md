---
UID: NF:ddraw.IDirectDrawSurface7.Blt
title: IDirectDrawSurface7::Blt (ddraw.h)
description: Performs a bit block transfer (bitblt). This method does not support z-buffering or alpha blending during bitblt operations.
helpviewer_keywords: ["All DDBLT_ALPHA flag values","All DDBLT_ZBUFFER flag values","Blt","Blt method [DirectDraw]","Blt method [DirectDraw]","IDirectDrawSurface7 interface","DDBLT_ASYNC","DDBLT_COLORFILL","DDBLT_DDFX","DDBLT_DDROPS","DDBLT_DEPTHFILL","DDBLT_DONOTWAIT","DDBLT_KEYDEST","DDBLT_KEYDESTOVERRIDE","DDBLT_KEYSRC","DDBLT_KEYSRCOVERRIDE","DDBLT_ROP","DDBLT_ROTATIONANGLE","DDBLT_WAIT","IDirectDrawSurface7 interface [DirectDraw]","Blt method","IDirectDrawSurface7.Blt","IDirectDrawSurface7::Blt","ddraw/IDirectDrawSurface7::Blt","directdraw.idirectdrawsurface7_blt"]
old-location: directdraw\idirectdrawsurface7_blt.htm
tech.root: directdraw
ms.assetid: e458c430-855c-419b-aa50-144d2b422e78
ms.date: 12/05/2018
ms.keywords: All DDBLT_ALPHA flag values, All DDBLT_ZBUFFER flag values, Blt, Blt method [DirectDraw], Blt method [DirectDraw],IDirectDrawSurface7 interface, DDBLT_ASYNC, DDBLT_COLORFILL, DDBLT_DDFX, DDBLT_DDROPS, DDBLT_DEPTHFILL, DDBLT_DONOTWAIT, DDBLT_KEYDEST, DDBLT_KEYDESTOVERRIDE, DDBLT_KEYSRC, DDBLT_KEYSRCOVERRIDE, DDBLT_ROP, DDBLT_ROTATIONANGLE, DDBLT_WAIT, IDirectDrawSurface7 interface [DirectDraw],Blt method, IDirectDrawSurface7.Blt, IDirectDrawSurface7::Blt, ddraw/IDirectDrawSurface7::Blt, directdraw.idirectdrawsurface7_blt
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawSurface7::Blt
 - ddraw/IDirectDrawSurface7::Blt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.Blt
---

# IDirectDrawSurface7::Blt


## -description

Performs a bit block transfer (bitblt). This method does not support z-buffering or alpha blending during bitblt operations.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <b>RECT</b> structure that defines the upper-left and lower-right points of the rectangle to bitblt to on the destination surface. If this parameter is NULL, the entire destination surface is used.

### -param unnamedParam2 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the DirectDrawSurface object that is the source of the bitblt.

### -param unnamedParam3 [in]

A pointer to a <b>RECT</b> structure that defines the upper-left and lower-right points of the rectangle to bitblt from on the source surface. If this parameter is NULL, the entire source surface is used.

### -param unnamedParam4 [in]

A combination of flags that determine the valid members of the associated <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure, specify color-key information, or request special behavior from the method. The following flags are defined:

<b>Validation flags</b>



#### DDBLT_COLORFILL

Uses the <b>dwFillColor</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the RGB color that fills the destination rectangle on the destination surface.



#### DDBLT_DDFX

Uses the <b>dwDDFX</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure to specify the effects to use for this bitblt.



#### DDBLT_DDROPS

Uses the <b>dwDDROP</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure to specify the raster operations (ROPS) that are not part of the Win32 API.



#### DDBLT_DEPTHFILL

Uses the <b>dwFillDepth</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the depth value with which to fill the destination rectangle on the destination z-buffer surface.



#### DDBLT_KEYDESTOVERRIDE

Uses the <b>ddckDestColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the color key for the destination surface.



#### DDBLT_KEYSRCOVERRIDE

Uses the <b>ddckSrcColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the color key for the source surface.



#### DDBLT_ROP

Uses the <b>dwROP</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure for the ROP for this bitblt. These ROPs are the same as those defined in the Win32 API.



#### DDBLT_ROTATIONANGLE

Uses the <b>dwRotationAngle</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the rotation angle (specified in 1/100s of a degree) for the surface.

<b>Color key flags</b>



#### DDBLT_KEYDEST

Uses the color key that is associated with the destination surface.



#### DDBLT_KEYSRC

Uses the color key that is associated with the source surface.

<b>Behavior flags</b>



#### DDBLT_ASYNC

Performs this bitblt asynchronously through the first in, first out (FIFO) hardware in the order received. If no room is available in the FIFO hardware, the call fails.



#### DDBLT_DONOTWAIT

Returns without bitbltting and also returns DDERR_WASSTILLDRAWING if the bitbltter is busy.



#### DDBLT_WAIT

Postpones the DDERR_WASSTILLDRAWING return value if the bitbltter is busy, and returns as soon as the bitblt can be set up or another error occurs.

<b>Obsolete and unsupported flags</b>



#### All DDBLT_ALPHA flag values

Not currently implemented.



#### All DDBLT_ZBUFFER flag values

This method does not currently support z-aware bitblt operations. None of the flags beginning with "DDBLT_ZBUFFER" are supported.

### -param unnamedParam5 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure for the bitblt.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOALPHAHW</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_NOCLIPLIST</li>
<li>DDERR_NODDROPSHW</li>
<li>DDERR_NOMIRRORHW</li>
<li>DDERR_NORASTEROPHW</li>
<li>DDERR_NOROTATIONHW</li>
<li>DDERR_NOSTRETCHHW</li>
<li>DDERR_NOZBUFFERHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks

<b>Blt</b> can perform synchronous or asynchronous bitblts (the latter is the default behavior). These bitblts can occur from display memory to display memory, from display memory to system memory, from system memory to display memory, or from system memory to system memory. The bitblts can be performed by using source color keys and destination color keys. Arbitrary stretching or shrinking is performed if the source and destination rectangles are not the same size.

Typically, <b>Blt</b> returns immediately with an error if the bitbltter is busy and the bitblt could not be set up. Specify the DDBLT_WAIT flag to request a synchronous bitblt. When you include the DDBLT_WAIT flag, <b>Blt</b> waits until the bitblt can be set up or another error occurs before it returns.

RECT structures are defined so that the right and bottom members are exclusive—therefore, right minus left equals the width of the rectangle, not 1 less than the width.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>