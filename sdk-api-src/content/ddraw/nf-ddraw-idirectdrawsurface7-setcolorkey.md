---
UID: NF:ddraw.IDirectDrawSurface7.SetColorKey
title: IDirectDrawSurface7::SetColorKey (ddraw.h)
description: Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.
helpviewer_keywords: ["DDCKEY_COLORSPACE","DDCKEY_DESTBLT","DDCKEY_DESTOVERLAY","DDCKEY_SRCBLT","DDCKEY_SRCOVERLAY","IDirectDrawSurface7 interface [DirectDraw]","SetColorKey method","IDirectDrawSurface7.SetColorKey","IDirectDrawSurface7::SetColorKey","SetColorKey","SetColorKey method [DirectDraw]","SetColorKey method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetColorKey","directdraw.idirectdrawsurface7_setcolorkey"]
old-location: directdraw\idirectdrawsurface7_setcolorkey.htm
tech.root: directdraw
ms.assetid: 36f2510e-d12a-40af-b65c-aa36ce46a942
ms.date: 12/05/2018
ms.keywords: DDCKEY_COLORSPACE, DDCKEY_DESTBLT, DDCKEY_DESTOVERLAY, DDCKEY_SRCBLT, DDCKEY_SRCOVERLAY, IDirectDrawSurface7 interface [DirectDraw],SetColorKey method, IDirectDrawSurface7.SetColorKey, IDirectDrawSurface7::SetColorKey, SetColorKey, SetColorKey method [DirectDraw], SetColorKey method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetColorKey, directdraw.idirectdrawsurface7_setcolorkey
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
 - IDirectDrawSurface7::SetColorKey
 - ddraw/IDirectDrawSurface7::SetColorKey
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
 - IDirectDrawSurface7.SetColorKey
---

# IDirectDrawSurface7::SetColorKey


## -description

Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.

## -parameters

### -param unnamedParam1 [in]

A value that can be set to one of the following flags to specify the requested color key:



#### DDCKEY_COLORSPACE

The structure contains a color space. Not set if the structure contains a single color key.



#### DDCKEY_DESTBLT

A color key or color space to be used as a destination color key for bit block transfer (bitblt) operations.



#### DDCKEY_DESTOVERLAY

A color key or color space to be used as a destination color key for overlay operations.



#### DDCKEY_SRCBLT

A color key or color space to be used as a source color key for bitblt operations.



#### DDCKEY_SRCOVERLAY

A color key or color space to be used as a source color key for overlay operations.

### -param unnamedParam2 [in]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcolorkey">DDCOLORKEY</a> structure that contains the new color key values for the DirectDrawSurface object. This value can be NULL to remove a previously set color key.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOOVERLAYHW</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>

## -remarks

For transparent bitblt operations and overlays, set destination color on the destination surface and source color on the source surface.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>