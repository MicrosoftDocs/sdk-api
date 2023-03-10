---
UID: NS:ddraw._DDBLTBATCH
title: DDBLTBATCH (ddraw.h)
description: The DDBLTBATCH structure passes bit block transfer (bitblt) operations to the IDirectDrawSurface7::BltBatch method.
helpviewer_keywords: ["*LPDDBLTBATCH","DDBLTBATCH","DDBLTBATCH structure [DirectDraw]","DDBLT_ALPHADEST","DDBLT_ALPHADESTCONSTOVERRIDE","DDBLT_ALPHADESTNEG","DDBLT_ALPHADESTSURFACEOVERRIDE","DDBLT_ALPHAEDGEBLEND","DDBLT_ALPHASRC","DDBLT_ALPHASRCCONSTOVERRIDE","DDBLT_ALPHASRCNEG","DDBLT_ALPHASRCSURFACEOVERRIDE","DDBLT_ASYNC","DDBLT_COLORFILL","DDBLT_DDFX","DDBLT_DDROPS","DDBLT_KEYDEST","DDBLT_KEYDESTOVERRIDE","DDBLT_KEYSRC","DDBLT_KEYSRCOVERRIDE","DDBLT_ROP","DDBLT_ROTATIONANGLE","DDBLT_ZBUFFER","DDBLT_ZBUFFERDESTCONSTOVERRIDE","DDBLT_ZBUFFERDESTOVERRIDE","DDBLT_ZBUFFERSRCCONSTOVERRIDE","DDBLT_ZBUFFERSRCOVERRIDE","LPDDBLTBATCH","LPDDBLTBATCH structure pointer [DirectDraw]","ddraw/DDBLTBATCH","ddraw/LPDDBLTBATCH","directdraw.ddbltbatch"]
old-location: directdraw\ddbltbatch.htm
tech.root: directdraw
ms.assetid: d8c302aa-9c57-41f8-ad22-d8fdd1158c3c
ms.date: 12/05/2018
ms.keywords: '*LPDDBLTBATCH, DDBLTBATCH, DDBLTBATCH structure [DirectDraw], DDBLT_ALPHADEST, DDBLT_ALPHADESTCONSTOVERRIDE, DDBLT_ALPHADESTNEG, DDBLT_ALPHADESTSURFACEOVERRIDE, DDBLT_ALPHAEDGEBLEND, DDBLT_ALPHASRC, DDBLT_ALPHASRCCONSTOVERRIDE, DDBLT_ALPHASRCNEG, DDBLT_ALPHASRCSURFACEOVERRIDE, DDBLT_ASYNC, DDBLT_COLORFILL, DDBLT_DDFX, DDBLT_DDROPS, DDBLT_KEYDEST, DDBLT_KEYDESTOVERRIDE, DDBLT_KEYSRC, DDBLT_KEYSRCOVERRIDE, DDBLT_ROP, DDBLT_ROTATIONANGLE, DDBLT_ZBUFFER, DDBLT_ZBUFFERDESTCONSTOVERRIDE, DDBLT_ZBUFFERDESTOVERRIDE, DDBLT_ZBUFFERSRCCONSTOVERRIDE, DDBLT_ZBUFFERSRCOVERRIDE, LPDDBLTBATCH, LPDDBLTBATCH structure pointer [DirectDraw], ddraw/DDBLTBATCH, ddraw/LPDDBLTBATCH, directdraw.ddbltbatch'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DDBLTBATCH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDBLTBATCH
 - ddraw/_DDBLTBATCH
 - DDBLTBATCH
 - ddraw/DDBLTBATCH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDBLTBATCH
---

# DDBLTBATCH structure


## -description

The DDBLTBATCH structure passes bit block transfer (bitblt) operations to the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a> method.

## -struct-fields

### -field lprDest

Address of a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the destination for the bitblt.

### -field lpDDSSrc

Address of a DirectDrawSurface object to be the source of the bitblt.

### -field lprSrc

Address of a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the source rectangle of the bitblt.

### -field dwFlags

Optional control flags. The following values are defined:



#### DDBLT_ALPHADEST

Uses either the alpha information in pixel format or the alpha channel surface attached to the destination surface as the alpha channel for this bitblt.



#### DDBLT_ALPHADESTCONSTOVERRIDE

Uses the <b>dwAlphaDestConst</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the alpha channel for the destination surface for this bitblt.



#### DDBLT_ALPHADESTNEG

The destination surface becomes more transparent as the alpha value increases (0 is opaque).



#### DDBLT_ALPHADESTSURFACEOVERRIDE

Uses the <b>lpDDSAlphaDest</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the alpha channel for the destination surface for this bitblt.



#### DDBLT_ALPHAEDGEBLEND

Uses the <b>dwAlphaEdgeBlend</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the alpha channel for the edges of the image that border the color key colors.



#### DDBLT_ALPHASRC

Uses either the alpha information in pixel format or the alpha channel surface attached to the source surface as the alpha channel for this bitblt.



#### DDBLT_ALPHASRCCONSTOVERRIDE

Uses the <b>dwAlphaSrcConst</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the source alpha channel for this bitblt.



#### DDBLT_ALPHASRCNEG

The source surface becomes more transparent as the alpha value increases (0 is opaque).



#### DDBLT_ALPHASRCSURFACEOVERRIDE

Uses the <b>lpDDSAlphaSrc</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the alpha channel source for this bitblt.



#### DDBLT_ASYNC

Performs this bitblt asynchronously through the first in, first out (FIFO) hardware in the order received. If no room is available in the FIFO hardware, the call fails.



#### DDBLT_COLORFILL

Uses the <b>dwFillColor</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the RGB color that fills the destination rectangle on the destination surface.



#### DDBLT_DDFX

Uses the <b>dwDDFX</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure to specify the effects to use for this bitblt.



#### DDBLT_DDROPS

Uses the <b>dwDDROP</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure to specify the raster operations (ROPS) that are not part of the Win32 API.



#### DDBLT_KEYDEST

Uses the color key that is associated with the destination surface.



#### DDBLT_KEYDESTOVERRIDE

Uses the <b>ddckDestColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the color key for the destination surface.



#### DDBLT_KEYSRC

Uses the color key that is associated with the source surface.



#### DDBLT_KEYSRCOVERRIDE

Uses the <b>ddckSrcColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the color key for the source surface.



#### DDBLT_ROP

Uses the <b>dwROP</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure for the ROP for this bitblt. These ROPs are the same as those defined in the Win32 API.



#### DDBLT_ROTATIONANGLE

Uses the <b>dwRotationAngle</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the rotation angle (specified in 1/100s of a degree) for the surface.



#### DDBLT_ZBUFFER

Performs a z-buffered bitblt, using the z-buffers that are attached to the source and destination surfaces and the <b>dwZBufferOpCode</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the z-buffer opcode.



#### DDBLT_ZBUFFERDESTCONSTOVERRIDE

Performs a z-buffered bitblt, using the <b>dwZDestConst</b> and <b>dwZBufferOpCode</b> members of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the z-buffer and z-buffer opcode, respectively, for the destination.



#### DDBLT_ZBUFFERDESTOVERRIDE

Performs a z-buffered bitblt, using the <b>lpDDSZBufferDest</b> and <b>dwZBufferOpCode</b> members of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the z-buffer and z-buffer opcode, respectively, for the destination.



#### DDBLT_ZBUFFERSRCCONSTOVERRIDE

Performs a z-buffered bitblt, using the <b>dwZSrcConst</b> and <b>dwZBufferOpCode</b> members of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the z-buffer and z-buffer opcode, respectively, for the source.



#### DDBLT_ZBUFFERSRCOVERRIDE

Performs a z-buffered bitblt, using the <b>lpDDSZBufferSrc</b> and <b>dwZBufferOpCode</b> members of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure as the z-buffer and z-buffer opcode, respectively, for the source.

### -field lpDDBltFx

Address of a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddbltfx">DDBLTFX</a> structure that specifies additional bitblt effects.