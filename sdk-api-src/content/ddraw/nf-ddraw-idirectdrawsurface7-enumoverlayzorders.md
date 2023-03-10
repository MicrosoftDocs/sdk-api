---
UID: NF:ddraw.IDirectDrawSurface7.EnumOverlayZOrders
title: IDirectDrawSurface7::EnumOverlayZOrders (ddraw.h)
description: Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.
helpviewer_keywords: ["DDENUMOVERLAYZ_BACKTOFRONT","DDENUMOVERLAYZ_FRONTTOBACK","EnumOverlayZOrders","EnumOverlayZOrders method [DirectDraw]","EnumOverlayZOrders method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","EnumOverlayZOrders method","IDirectDrawSurface7.EnumOverlayZOrders","IDirectDrawSurface7::EnumOverlayZOrders","ddraw/IDirectDrawSurface7::EnumOverlayZOrders","directdraw.idirectdrawsurface7_enumoverlayzorders"]
old-location: directdraw\idirectdrawsurface7_enumoverlayzorders.htm
tech.root: directdraw
ms.assetid: fab3212c-c1af-4119-85ff-108594cc64fa
ms.date: 12/05/2018
ms.keywords: DDENUMOVERLAYZ_BACKTOFRONT, DDENUMOVERLAYZ_FRONTTOBACK, EnumOverlayZOrders, EnumOverlayZOrders method [DirectDraw], EnumOverlayZOrders method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],EnumOverlayZOrders method, IDirectDrawSurface7.EnumOverlayZOrders, IDirectDrawSurface7::EnumOverlayZOrders, ddraw/IDirectDrawSurface7::EnumOverlayZOrders, directdraw.idirectdrawsurface7_enumoverlayzorders
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
 - IDirectDrawSurface7::EnumOverlayZOrders
 - ddraw/IDirectDrawSurface7::EnumOverlayZOrders
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
 - IDirectDrawSurface7.EnumOverlayZOrders
---

# IDirectDrawSurface7::EnumOverlayZOrders


## -description

Enumerates the overlay surfaces on the specified destination. You can enumerate the overlays in front-to-back or back-to-front order.

## -parameters

### -param unnamedParam1 [in]

A value that can be set to one of the following flags:



#### DDENUMOVERLAYZ_BACKTOFRONT

Enumerates overlays back to front.



#### DDENUMOVERLAYZ_FRONTTOBACK

Enumerates overlays front to back.

### -param unnamedParam2 [in]

Address of the user-defined structure to be passed to the callback function for each overlay surface.

### -param unnamedParam3 [in]

Address of the <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> callback function to be called for each surface to be overlaid on this surface.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

<b>EnumOverlayZOrders</b> differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function, rather than an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback">EnumSurfacesCallback</a> or <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback2">EnumSurfacesCallback2</a> function.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>