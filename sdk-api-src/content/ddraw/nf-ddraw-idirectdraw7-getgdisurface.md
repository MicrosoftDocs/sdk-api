---
UID: NF:ddraw.IDirectDraw7.GetGDISurface
title: IDirectDraw7::GetGDISurface (ddraw.h)
description: Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.
helpviewer_keywords: ["GetGDISurface","GetGDISurface method [DirectDraw]","GetGDISurface method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetGDISurface method","IDirectDraw7.GetGDISurface","IDirectDraw7::GetGDISurface","ddraw/IDirectDraw7::GetGDISurface","directdraw.idirectdraw7_getgdisurface"]
old-location: directdraw\idirectdraw7_getgdisurface.htm
tech.root: directdraw
ms.assetid: 4d0b827d-86f8-4d71-a193-9e330db0fbfd
ms.date: 12/05/2018
ms.keywords: GetGDISurface, GetGDISurface method [DirectDraw], GetGDISurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetGDISurface method, IDirectDraw7.GetGDISurface, IDirectDraw7::GetGDISurface, ddraw/IDirectDraw7::GetGDISurface, directdraw.idirectdraw7_getgdisurface
f1_keywords:
- ddraw/IDirectDraw7.GetGDISurface
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
- IDirectDraw7.GetGDISurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.

## -parameters

### -param unnamedParam1 [out]

Address of a variable to be filled with a pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the surface that currently controls the GDI's primary surface memory.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>