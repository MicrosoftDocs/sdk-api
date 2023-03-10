---
UID: NF:ddraw.IDirectDraw7.FlipToGDISurface
title: IDirectDraw7::FlipToGDISurface (ddraw.h)
description: Makes the surface that the GDI writes to the primary surface.
helpviewer_keywords: ["FlipToGDISurface","FlipToGDISurface method [DirectDraw]","FlipToGDISurface method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","FlipToGDISurface method","IDirectDraw7.FlipToGDISurface","IDirectDraw7::FlipToGDISurface","ddraw/IDirectDraw7::FlipToGDISurface","directdraw.idirectdraw7_fliptogdisurface"]
old-location: directdraw\idirectdraw7_fliptogdisurface.htm
tech.root: directdraw
ms.assetid: 495cace2-a315-4937-b0d9-9f77f5d95f66
ms.date: 12/05/2018
ms.keywords: FlipToGDISurface, FlipToGDISurface method [DirectDraw], FlipToGDISurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],FlipToGDISurface method, IDirectDraw7.FlipToGDISurface, IDirectDraw7::FlipToGDISurface, ddraw/IDirectDraw7::FlipToGDISurface, directdraw.idirectdraw7_fliptogdisurface
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
 - IDirectDraw7::FlipToGDISurface
 - ddraw/IDirectDraw7::FlipToGDISurface
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
 - IDirectDraw7.FlipToGDISurface
---

# IDirectDraw7::FlipToGDISurface


## -description

Makes the surface that the GDI writes to the primary surface.



## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>

## -remarks

You can call  <b>FlipToGDISurface</b> at the end of a page-flipping application to ensure that the display memory that the GDI writes to is visible.

You can also use  <b>FlipToGDISurface</b> to make the GDI surface the primary surface so that normal windows, such as dialog boxes, can be displayed in full-screen mode. The hardware must have the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS2_CANRENDERWINDOWED</a> capability.

<b>FlipToGDISurface</b> disables stereo autoflipping.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
