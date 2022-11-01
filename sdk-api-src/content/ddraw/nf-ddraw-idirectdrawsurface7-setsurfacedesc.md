---
UID: NF:ddraw.IDirectDrawSurface7.SetSurfaceDesc
title: IDirectDrawSurface7::SetSurfaceDesc (ddraw.h)
description: Sets the characteristics of an existing surface.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetSurfaceDesc method","IDirectDrawSurface7.SetSurfaceDesc","IDirectDrawSurface7::SetSurfaceDesc","SetSurfaceDesc","SetSurfaceDesc method [DirectDraw]","SetSurfaceDesc method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetSurfaceDesc","directdraw.idirectdrawsurface7_setsurfacedesc"]
old-location: directdraw\idirectdrawsurface7_setsurfacedesc.htm
tech.root: directdraw
ms.assetid: 541bd833-20c4-4b47-a3ed-c29f228a0626
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetSurfaceDesc method, IDirectDrawSurface7.SetSurfaceDesc, IDirectDrawSurface7::SetSurfaceDesc, SetSurfaceDesc, SetSurfaceDesc method [DirectDraw], SetSurfaceDesc method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetSurfaceDesc, directdraw.idirectdrawsurface7_setsurfacedesc
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
 - IDirectDrawSurface7::SetSurfaceDesc
 - ddraw/IDirectDrawSurface7::SetSurfaceDesc
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
 - IDirectDrawSurface7.SetSurfaceDesc
---

# IDirectDrawSurface7::SetSurfaceDesc


## -description

Sets the characteristics of an existing surface.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that contains the new surface characteristics.

### -param unnamedParam2 [in]

Currently not used and must be set to 0.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_GENERIC</li>
</ul>

## -remarks

Currently, you can use <b>SetSurfaceDesc</b> only to set the surface data and pixel format that is used by an explicit system-memory surface. This is useful because it allows a surface to use data from a previously allocated buffer without copying. The new surface memory is allocated by the client application, and therefore the client application must also deallocate it.

The DirectDrawSurface object does not deallocate surface memory that it did not allocate. Therefore, when the surface memory is no longer needed, you must deallocate it. However, when you call <b>SetSurfaceDesc</b>, DirectDraw frees the original surface memory that it implicitly allocated when it created the surface.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>