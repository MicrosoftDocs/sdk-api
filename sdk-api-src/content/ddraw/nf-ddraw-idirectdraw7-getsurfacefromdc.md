---
UID: NF:ddraw.IDirectDraw7.GetSurfaceFromDC
title: IDirectDraw7::GetSurfaceFromDC (ddraw.h)
description: Retrieves the IDirectDrawSurface7 interface for a surface, based on its GDI device context handle.
helpviewer_keywords: ["GetSurfaceFromDC","GetSurfaceFromDC method [DirectDraw]","GetSurfaceFromDC method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","GetSurfaceFromDC method","IDirectDraw7.GetSurfaceFromDC","IDirectDraw7::GetSurfaceFromDC","ddraw/IDirectDraw7::GetSurfaceFromDC","directdraw.idirectdraw7_getsurfacefromdc"]
old-location: directdraw\idirectdraw7_getsurfacefromdc.htm
tech.root: directdraw
ms.assetid: d1d96045-a19b-46b0-8b71-5d0bea6889c3
ms.date: 12/05/2018
ms.keywords: GetSurfaceFromDC, GetSurfaceFromDC method [DirectDraw], GetSurfaceFromDC method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetSurfaceFromDC method, IDirectDraw7.GetSurfaceFromDC, IDirectDraw7::GetSurfaceFromDC, ddraw/IDirectDraw7::GetSurfaceFromDC, directdraw.idirectdraw7_getsurfacefromdc
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
 - IDirectDraw7::GetSurfaceFromDC
 - ddraw/IDirectDraw7::GetSurfaceFromDC
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
 - IDirectDraw7.GetSurfaceFromDC
---

# IDirectDraw7::GetSurfaceFromDC


## -description

Retrieves the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for a surface, based on its GDI device context handle.

## -parameters

### -param unnamedParam1 [in]

Handle of a display device context.

### -param unnamedParam2 [out]

Address of a variable to be filled with a pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the surface if the call succeeds.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_NOTFOUND</li>
</ul>

## -remarks

This method succeeds only for device context handles that identify surfaces already associated with the DirectDraw object.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>