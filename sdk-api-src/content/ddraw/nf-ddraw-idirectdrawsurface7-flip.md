---
UID: NF:ddraw.IDirectDrawSurface7.Flip
title: IDirectDrawSurface7::Flip (ddraw.h)
description: Makes the surface memory that is associated with the DDSCAPS_BACKBUFFER surface become associated with the front-buffer surface.
helpviewer_keywords: ["DDFLIP_DONOTWAIT","DDFLIP_EVEN","DDFLIP_INTERVAL2","DDFLIP_INTERVAL3","DDFLIP_INTERVAL4","DDFLIP_NOVSYNC","DDFLIP_ODD","DDFLIP_STEREO","DDFLIP_WAIT","Flip","Flip method [DirectDraw]","Flip method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","Flip method","IDirectDrawSurface7.Flip","IDirectDrawSurface7::Flip","ddraw/IDirectDrawSurface7::Flip","directdraw.idirectdrawsurface7_flip"]
old-location: directdraw\idirectdrawsurface7_flip.htm
tech.root: directdraw
ms.assetid: 6c0c23e7-7567-4e07-9ba0-5e50b758f711
ms.date: 12/05/2018
ms.keywords: DDFLIP_DONOTWAIT, DDFLIP_EVEN, DDFLIP_INTERVAL2, DDFLIP_INTERVAL3, DDFLIP_INTERVAL4, DDFLIP_NOVSYNC, DDFLIP_ODD, DDFLIP_STEREO, DDFLIP_WAIT, Flip, Flip method [DirectDraw], Flip method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],Flip method, IDirectDrawSurface7.Flip, IDirectDrawSurface7::Flip, ddraw/IDirectDrawSurface7::Flip, directdraw.idirectdrawsurface7_flip
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
 - IDirectDrawSurface7::Flip
 - ddraw/IDirectDrawSurface7::Flip
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
 - IDirectDrawSurface7.Flip
---

# IDirectDrawSurface7::Flip


## -description

Makes the surface memory that is associated with the DDSCAPS_BACKBUFFER surface become associated with the front-buffer surface.

## -parameters

### -param unnamedParam1 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for an arbitrary surface in the flipping chain. The default for this parameter is NULL, in which case DirectDraw cycles through the buffers in the order that they are attached to each other. If this parameter is not NULL, DirectDraw flips to the specified surface, instead of the next surface in the flipping chain. <b>Flip</b> fails if the specified surface is not a member of the flipping chain.

### -param unnamedParam2 [in]

A combination of flags that specify flip options. The following flags are defined:



#### DDFLIP_DONOTWAIT

On <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interfaces, the default is DDFLIP_WAIT. If you want to override the default and use time when the accelerator is busy (as denoted by the DDERR_WASSTILLDRAWING return value), use DDFLIP_DONOTWAIT.



#### DDFLIP_EVEN

For use only when displaying video in an overlay surface. The new surface contains data from the even field of a video signal. This flag cannot be used with the DDFLIP_ODD flag.



#### DDFLIP_STEREO

DirectDraw flips and displays a main stereo surface. When this flag is set, stereo autoflipping is enabled. The hardware automatically flips between the left and right buffers during each screen refresh.



#### DDFLIP_INTERVAL2



#### DDFLIP_INTERVAL3



#### DDFLIP_INTERVAL4

The DDFLIP_INTERVAL2, DDFLIP_INTERVAL3, and DDFLIP_INTERVAL4 flags indicate how many vertical retraces to wait between each flip. The default is 1. DirectDraw returns DERR_WASSTILLDRAWING for each surface involved in the flip until the specified number of vertical retraces has occurred. If DDFLIP_INTERVAL2 is set, DirectDraw flips on every second vertical sync; if DDFLIP_INTERVAL3, on every third sync; and if DDFLIP_INTERVAL4, on every fourth sync.

These flags are effective only if DDCAPS2_FLIPINTERVAL bit is set in the  <b>dwCaps2</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure that is returned for the display hardware.



#### DDFLIP_NOVSYNC

Causes DirectDraw to perform the physical flip as close as possible to the next scan line. Subsequent operations that involve the two flipped surfaces do not check whether the physical flip has finished—that is, they do not return DDERR_WASSTILLDRAWING for that reason (but might for other reasons). This allows an application to perform flips at a higher frequency than the monitor refresh rate, but might introduce visible artifacts.

If DDCAPS2_FLIPNOVSYNC is not set in the <b>dwCaps2</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure that is returned for the display hardware, DDFLIP_NOVSYNC has no effect.



#### DDFLIP_ODD

For use only when displaying video in an overlay surface. The new surface contains data from the odd field of a video signal. This flag cannot be used with the DDFLIP_EVEN flag.



#### DDFLIP_WAIT

Typically, if the flip cannot be set up because the state of the display hardware is not appropriate, the DDERR_WASSTILLDRAWING error returns immediately, and no flip occurs. Setting this flag causes <b>Flip</b> to continue trying to flip if it receives the DDERR_WASSTILLDRAWING error from the hardware abstraction layer (HAL). <b>Flip</b> does not return until the flipping operation has been successfully set up or another error, such as DDERR_SURFACEBUSY, is returned.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOFLIPHW</li>
<li>DDERR_NOTFLIPPABLE</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks

With <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>, the default behavior of <b>Flip</b> is to wait for the accelerator to finish. Therefore, under default conditions, <b>Flip</b> never returns DDERR_WASSTILLDRAWING. If you want to see the error codes and not wait until the flip operation succeeds, use the DDFLIP_DONOTWAIT flag.



<b>Flip</b> can be called only for a surface that has the DDSCAPS_FLIP and DDSCAPS_FRONTBUFFER capabilities. The display memory previously associated with the front buffer is associated with the back buffer.



The <i>lpDDSurfaceTargetOverride</i> parameter is used in rare cases in which the back buffer is not the buffer that should become the front buffer. Typically, this parameter is NULL.

<b>Flip</b> is always synchronized with the vertical blank. If the surface has been assigned to a video port, this method updates the visible overlay surface and the target surface of the video port.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>