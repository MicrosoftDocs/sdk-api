---
UID: NF:ddraw.IDirectDrawSurface7.GetPalette
title: IDirectDrawSurface7::GetPalette (ddraw.h)
description: Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.
helpviewer_keywords: ["GetPalette","GetPalette method [DirectDraw]","GetPalette method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetPalette method","IDirectDrawSurface7.GetPalette","IDirectDrawSurface7::GetPalette","ddraw/IDirectDrawSurface7::GetPalette","directdraw.idirectdrawsurface7_getpalette"]
old-location: directdraw\idirectdrawsurface7_getpalette.htm
tech.root: directdraw
ms.assetid: 35a667aa-9a69-4c71-9e26-b42359815a0d
ms.date: 12/05/2018
ms.keywords: GetPalette, GetPalette method [DirectDraw], GetPalette method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPalette method, IDirectDrawSurface7.GetPalette, IDirectDrawSurface7::GetPalette, ddraw/IDirectDrawSurface7::GetPalette, directdraw.idirectdrawsurface7_getpalette
f1_keywords:
- ddraw/IDirectDrawSurface7.GetPalette
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
- IDirectDrawSurface7.GetPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable to receive a pointer to the palette object's <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a> interface.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOPALETTEATTACHED</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>