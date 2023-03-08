---
UID: NF:ddraw.IDirectDrawSurface7.GetPixelFormat
title: IDirectDrawSurface7::GetPixelFormat (ddraw.h)
description: Retrieves the color and pixel format of this surface.
helpviewer_keywords: ["GetPixelFormat","GetPixelFormat method [DirectDraw]","GetPixelFormat method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetPixelFormat method","IDirectDrawSurface7.GetPixelFormat","IDirectDrawSurface7::GetPixelFormat","ddraw/IDirectDrawSurface7::GetPixelFormat","directdraw.idirectdrawsurface7_getpixelformat"]
old-location: directdraw\idirectdrawsurface7_getpixelformat.htm
tech.root: directdraw
ms.assetid: 2c33c46b-6cd7-4ee7-976c-a81f9d92b379
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [DirectDraw], GetPixelFormat method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPixelFormat method, IDirectDrawSurface7.GetPixelFormat, IDirectDrawSurface7::GetPixelFormat, ddraw/IDirectDrawSurface7::GetPixelFormat, directdraw.idirectdrawsurface7_getpixelformat
f1_keywords:
- ddraw/IDirectDrawSurface7.GetPixelFormat
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
- IDirectDrawSurface7.GetPixelFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the color and pixel format of this surface.

## -parameters

### -param unnamedParam1 [out]

A pointer to a <a href="/windows/desktop/api/ddraw/ns-ddraw-ddpixelformat">DDPIXELFORMAT</a> structure that receives a detailed description of the current pixel and color space format of this surface.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>