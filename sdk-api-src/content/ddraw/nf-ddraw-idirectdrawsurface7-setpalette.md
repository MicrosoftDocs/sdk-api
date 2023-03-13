---
UID: NF:ddraw.IDirectDrawSurface7.SetPalette
title: IDirectDrawSurface7::SetPalette (ddraw.h)
description: Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetPalette method","IDirectDrawSurface7.SetPalette","IDirectDrawSurface7::SetPalette","SetPalette","SetPalette method [DirectDraw]","SetPalette method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetPalette","directdraw.idirectdrawsurface7_setpalette"]
old-location: directdraw\idirectdrawsurface7_setpalette.htm
tech.root: directdraw
ms.assetid: 938906fe-9f5b-468b-8b34-5de16aeb67b3
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetPalette method, IDirectDrawSurface7.SetPalette, IDirectDrawSurface7::SetPalette, SetPalette, SetPalette method [DirectDraw], SetPalette method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetPalette, directdraw.idirectdrawsurface7_setpalette
f1_keywords:
- ddraw/IDirectDrawSurface7.SetPalette
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDrawSurface7.SetPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing.

## -parameters

### -param unnamedParam1 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a> interface for the palette object to be used with this surface. If NULL, the current palette is detached.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOPALETTEATTACHED</li>
<li>DDERR_NOPALETTEHW</li>
<li>DDERR_NOT8BITCOLOR</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks

When you call <b>SetPalette</b> to  set a palette to a surface for the first time, <b>SetPalette</b> increments the palette's reference count; subsequent calls to <b>SetPalette</b> do not affect the palette's reference count. If you pass NULL as the <i>lpDDPalette</i> parameter, the palette is removed from the surface, and the palette's reference count is decremented. If you do not delete the palette, the surface automatically releases its reference to the palette when the surface itself is released. According to COM rules, your application must release any references that it holds to the palette when the object is no longer needed.



## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 