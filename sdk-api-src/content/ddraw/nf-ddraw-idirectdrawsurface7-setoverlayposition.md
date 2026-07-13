---
UID: NF:ddraw.IDirectDrawSurface7.SetOverlayPosition
title: IDirectDrawSurface7::SetOverlayPosition (ddraw.h)
description: Changes the display coordinates of an overlay surface.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetOverlayPosition method","IDirectDrawSurface7.SetOverlayPosition","IDirectDrawSurface7::SetOverlayPosition","SetOverlayPosition","SetOverlayPosition method [DirectDraw]","SetOverlayPosition method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetOverlayPosition","directdraw.idirectdrawsurface7_setoverlayposition"]
old-location: directdraw\idirectdrawsurface7_setoverlayposition.htm
tech.root: directdraw
ms.assetid: 94bd79f8-ded2-4cfa-98c1-a03202d3e678
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetOverlayPosition method, IDirectDrawSurface7.SetOverlayPosition, IDirectDrawSurface7::SetOverlayPosition, SetOverlayPosition, SetOverlayPosition method [DirectDraw], SetOverlayPosition method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetOverlayPosition, directdraw.idirectdrawsurface7_setoverlayposition
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
 - IDirectDrawSurface7::SetOverlayPosition
 - ddraw/IDirectDrawSurface7::SetOverlayPosition
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
 - IDirectDrawSurface7.SetOverlayPosition
---

# IDirectDrawSurface7::SetOverlayPosition


## -description

Changes the display coordinates of an overlay surface.

## -parameters

### -param unnamedParam1 [in]

The new x- display coordinate of this surface.

### -param unnamedParam2 [in]

The new y-display coordinate of this surface.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPOSITION</li>
<li>DDERR_NOOVERLAYDEST</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_OVERLAYNOTVISIBLE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>