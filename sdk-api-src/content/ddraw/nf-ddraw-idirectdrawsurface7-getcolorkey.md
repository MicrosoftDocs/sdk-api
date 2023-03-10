---
UID: NF:ddraw.IDirectDrawSurface7.GetColorKey
title: IDirectDrawSurface7::GetColorKey (ddraw.h)
description: Retrieves the color key value for this surface.
helpviewer_keywords: ["DDCKEY_DESTBLT","DDCKEY_DESTOVERLAY","DDCKEY_SRCBLT","DDCKEY_SRCOVERLAY","GetColorKey","GetColorKey method [DirectDraw]","GetColorKey method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetColorKey method","IDirectDrawSurface7.GetColorKey","IDirectDrawSurface7::GetColorKey","ddraw/IDirectDrawSurface7::GetColorKey","directdraw.idirectdrawsurface7_getcolorkey"]
old-location: directdraw\idirectdrawsurface7_getcolorkey.htm
tech.root: directdraw
ms.assetid: 0df14c63-f962-4823-873a-3fe1d626f4cb
ms.date: 12/05/2018
ms.keywords: DDCKEY_DESTBLT, DDCKEY_DESTOVERLAY, DDCKEY_SRCBLT, DDCKEY_SRCOVERLAY, GetColorKey, GetColorKey method [DirectDraw], GetColorKey method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetColorKey method, IDirectDrawSurface7.GetColorKey, IDirectDrawSurface7::GetColorKey, ddraw/IDirectDrawSurface7::GetColorKey, directdraw.idirectdrawsurface7_getcolorkey
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
 - IDirectDrawSurface7::GetColorKey
 - ddraw/IDirectDrawSurface7::GetColorKey
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
 - IDirectDrawSurface7.GetColorKey
---

# IDirectDrawSurface7::GetColorKey


## -description

Retrieves the color key value for this surface.

## -parameters

### -param unnamedParam1 [in]

A value that can be set to one of the following flags to specify the color key to retrieve:



#### DDCKEY_DESTBLT

A color key or color space to be used as a destination color key for bit block transfer (bitblt) operations.



#### DDCKEY_DESTOVERLAY

A color key or color space to be used as a destination color key for overlay operations.



#### DDCKEY_SRCBLT

A color key or color space to be used as a source color key for bitblt operations.



#### DDCKEY_SRCOVERLAY

A color key or color space to be used as a source color key for overlay operations.

### -param unnamedParam2 [out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcolorkey">DDCOLORKEY</a> structure that receives the current values for the specified color key of the DirectDrawSurface object.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCOLORKEY</li>
<li>DDERR_NOCOLORKEYHW</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>