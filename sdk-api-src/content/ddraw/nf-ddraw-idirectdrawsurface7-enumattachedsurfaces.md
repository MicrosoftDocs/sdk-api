---
UID: NF:ddraw.IDirectDrawSurface7.EnumAttachedSurfaces
title: IDirectDrawSurface7::EnumAttachedSurfaces (ddraw.h)
description: Enumerates all the surfaces that are attached to this surface.
helpviewer_keywords: ["EnumAttachedSurfaces","EnumAttachedSurfaces method [DirectDraw]","EnumAttachedSurfaces method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","EnumAttachedSurfaces method","IDirectDrawSurface7.EnumAttachedSurfaces","IDirectDrawSurface7::EnumAttachedSurfaces","ddraw/IDirectDrawSurface7::EnumAttachedSurfaces","directdraw.idirectdrawsurface7_enumattachedsurfaces"]
old-location: directdraw\idirectdrawsurface7_enumattachedsurfaces.htm
tech.root: directdraw
ms.assetid: 7f8e9b53-3aff-491c-ab0c-2f414d1ddb27
ms.date: 12/05/2018
ms.keywords: EnumAttachedSurfaces, EnumAttachedSurfaces method [DirectDraw], EnumAttachedSurfaces method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],EnumAttachedSurfaces method, IDirectDrawSurface7.EnumAttachedSurfaces, IDirectDrawSurface7::EnumAttachedSurfaces, ddraw/IDirectDrawSurface7::EnumAttachedSurfaces, directdraw.idirectdrawsurface7_enumattachedsurfaces
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
 - IDirectDrawSurface7::EnumAttachedSurfaces
 - ddraw/IDirectDrawSurface7::EnumAttachedSurfaces
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
 - IDirectDrawSurface7.EnumAttachedSurfaces
---

# IDirectDrawSurface7::EnumAttachedSurfaces


## -description

Enumerates all the surfaces that are attached to this surface.

## -parameters

### -param unnamedParam1 [in]

Address of the application-defined structure that is passed to the enumeration member every time that it is called.

### -param unnamedParam2 [in]

Address of the <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function to be called for each surface that is attached to this surface.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

<b>EnumAttachedSurfaces</b> enumerates only those surfaces that are directly attached to this surface. For example, in a flipping chain of three or more surfaces, only one surface is enumerated because each surface is attached only to the next surface in the flipping chain. In such a configuration, you can call <b>EnumAttachedSurfaces</b> on each successive surface to walk the entire flipping chain.

<b>EnumAttachedSurfaces</b> differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback7">EnumSurfacesCallback7</a> function, rather than an <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback">EnumSurfacesCallback</a> or <a href="/windows/desktop/api/ddraw/nc-ddraw-lpddenumsurfacescallback2">EnumSurfacesCallback2</a> function.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>