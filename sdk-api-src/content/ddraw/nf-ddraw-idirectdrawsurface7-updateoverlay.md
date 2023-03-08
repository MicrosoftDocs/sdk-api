---
UID: NF:ddraw.IDirectDrawSurface7.UpdateOverlay
title: IDirectDrawSurface7::UpdateOverlay (ddraw.h)
description: Repositions or modifies the visual attributes of an overlay surface. These surfaces must have the DDSCAPS_OVERLAY flag set.
helpviewer_keywords: ["DDOVER_ADDDIRTYRECT","DDOVER_ALPHADEST","DDOVER_ALPHADESTCONSTOVERRIDE","DDOVER_ALPHADESTNEG","DDOVER_ALPHADESTSURFACEOVERRIDE","DDOVER_ALPHAEDGEBLEND","DDOVER_ALPHASRC","DDOVER_ALPHASRCCONSTOVERRIDE","DDOVER_ALPHASRCNEG","DDOVER_ALPHASRCSURFACEOVERRIDE","DDOVER_ARGBSCALEFACTORS","DDOVER_AUTOFLIP","DDOVER_BOB","DDOVER_BOBHARDWARE","DDOVER_DDFX","DDOVER_DEGRADEARGBSCALING","DDOVER_HIDE","DDOVER_INTERLEAVED","DDOVER_KEYDEST","DDOVER_KEYDESTOVERRIDE","DDOVER_KEYSRC","DDOVER_KEYSRCOVERRIDE","DDOVER_OVERRIDEBOBWEAVE","DDOVER_REFRESHALL","DDOVER_REFRESHDIRTYRECTS","DDOVER_SHOW","IDirectDrawSurface7 interface [DirectDraw]","UpdateOverlay method","IDirectDrawSurface7.UpdateOverlay","IDirectDrawSurface7::UpdateOverlay","UpdateOverlay","UpdateOverlay method [DirectDraw]","UpdateOverlay method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::UpdateOverlay","directdraw.idirectdrawsurface7_updateoverlay"]
old-location: directdraw\idirectdrawsurface7_updateoverlay.htm
tech.root: directdraw
ms.assetid: 8706c6ca-cd17-490a-8ff9-9470a7d7a150
ms.date: 12/05/2018
ms.keywords: DDOVER_ADDDIRTYRECT, DDOVER_ALPHADEST, DDOVER_ALPHADESTCONSTOVERRIDE, DDOVER_ALPHADESTNEG, DDOVER_ALPHADESTSURFACEOVERRIDE, DDOVER_ALPHAEDGEBLEND, DDOVER_ALPHASRC, DDOVER_ALPHASRCCONSTOVERRIDE, DDOVER_ALPHASRCNEG, DDOVER_ALPHASRCSURFACEOVERRIDE, DDOVER_ARGBSCALEFACTORS, DDOVER_AUTOFLIP, DDOVER_BOB, DDOVER_BOBHARDWARE, DDOVER_DDFX, DDOVER_DEGRADEARGBSCALING, DDOVER_HIDE, DDOVER_INTERLEAVED, DDOVER_KEYDEST, DDOVER_KEYDESTOVERRIDE, DDOVER_KEYSRC, DDOVER_KEYSRCOVERRIDE, DDOVER_OVERRIDEBOBWEAVE, DDOVER_REFRESHALL, DDOVER_REFRESHDIRTYRECTS, DDOVER_SHOW, IDirectDrawSurface7 interface [DirectDraw],UpdateOverlay method, IDirectDrawSurface7.UpdateOverlay, IDirectDrawSurface7::UpdateOverlay, UpdateOverlay, UpdateOverlay method [DirectDraw], UpdateOverlay method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::UpdateOverlay, directdraw.idirectdrawsurface7_updateoverlay
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
 - IDirectDrawSurface7::UpdateOverlay
 - ddraw/IDirectDrawSurface7::UpdateOverlay
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
 - IDirectDrawSurface7.UpdateOverlay
---

# IDirectDrawSurface7::UpdateOverlay


## -description

Repositions or modifies the visual attributes of an overlay surface. These surfaces must have the DDSCAPS_OVERLAY flag set.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <b>RECT</b> structure that defines the x, y, width, and height of the region on the source surface being used as the overlay. This parameter can be NULL to hide an overlay or to indicate that the entire overlay surface is to be used and that the overlay surface conforms to any boundary and size-alignment restrictions imposed by the device driver.

### -param unnamedParam2 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the DirectDrawSurface object that is being overlaid.

### -param unnamedParam3 [in]

A pointer to a <b>RECT</b> structure that defines the width, x, and height, y, of the region on the destination surface that the overlay should be moved to. This parameter can be NULL to hide the overlay.

### -param unnamedParam4 [in]

A combination of the following flags that determine the overlay update:



#### DDOVER_ADDDIRTYRECT

Adds a dirty rectangle to an emulated overlay surface.



#### DDOVER_ALPHADEST

Obsolete.



#### DDOVER_ALPHADESTCONSTOVERRIDE

Uses the <b>dwAlphaDestConst</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the destination alpha channel for this overlay.



#### DDOVER_ALPHADESTNEG

Indicates that the destination surface becomes more transparent as the alpha value increases (0 is opaque).



#### DDOVER_ALPHADESTSURFACEOVERRIDE

Uses the <b>lpDDSAlphaDest</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the alpha channel destination for this overlay.



#### DDOVER_ALPHAEDGEBLEND

Uses the <b>dwAlphaEdgeBlend</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the alpha channel for the edges of the image that border the color key colors.



#### DDOVER_ALPHASRC

Uses either the alpha information in pixel format or the alpha channel surface attached to the source surface as the source alpha channel for this overlay.



#### DDOVER_ALPHASRCCONSTOVERRIDE

Uses the <b>dwAlphaSrcConst</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the source alpha channel for this overlay.



#### DDOVER_ALPHASRCNEG

Indicates that the source surface becomes more transparent as the alpha value increases (0 is opaque). 




#### DDOVER_ALPHASRCSURFACEOVERRIDE

Uses the <b>lpDDSAlphaSrc</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the alpha channel source for this overlay.



#### DDOVER_ARGBSCALEFACTORS

New for DirectX 7.0. Indicates that the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure contains valid ARGB scaling factors.



#### DDOVER_AUTOFLIP

Automatically flips to the next surface in the flipping chain each time that a video port VSYNC occurs.



#### DDOVER_BOB

Displays each field of the interlaced video stream individually without causing any artifacts to display.



#### DDOVER_BOBHARDWARE

Bob operations are performed by using hardware, rather than by using software or being emulated. This flag must be used with the DDOVER_BOB flag.



#### DDOVER_DDFX

Uses the overlay FX flags in the <i>lpDDOverlayFx</i> parameter to define special overlay effects.



#### DDOVER_DEGRADEARGBSCALING

New for DirectX 7.0. ARGB scaling factors can be degraded to fit driver capabilities.



#### DDOVER_HIDE

Turns off this overlay.



#### DDOVER_INTERLEAVED

The surface memory is composed of interleaved fields.



#### DDOVER_KEYDEST

Uses the color key associated with the destination surface.



#### DDOVER_KEYDESTOVERRIDE

Uses the <b>dckDestColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the color key for the destination surface.



#### DDOVER_KEYSRC

Uses the color key associated with the source surface.



#### DDOVER_KEYSRCOVERRIDE

Uses the <b>dckSrcColorkey</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure as the color key for the source surface.



#### DDOVER_OVERRIDEBOBWEAVE

Bob and weave decisions should not be overridden by other interfaces.



#### DDOVER_REFRESHALL

Redraws the entire surface on an emulated overlayed surface.



#### DDOVER_REFRESHDIRTYRECTS

Redraws all dirty rectangles on an emulated overlayed surface.



#### DDOVER_SHOW

Turns on this overlay.

### -param unnamedParam5 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddoverlayfx">DDOVERLAYFX</a> structure that describes the effects to be used. Can be NULL if the DDOVER_DDFX flag is not specified.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_DEVICEDOESNTOWNSURFACE</li>
<li>DDERR_GENERIC</li>
<li>DDERR_HEIGHTALIGN</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOSTRETCHHW</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_OUTOFCAPS</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_XALIGN</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>