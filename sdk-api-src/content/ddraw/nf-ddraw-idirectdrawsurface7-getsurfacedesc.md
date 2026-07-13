---
UID: NF:ddraw.IDirectDrawSurface7.GetSurfaceDesc
title: IDirectDrawSurface7::GetSurfaceDesc (ddraw.h)
description: Retrieves a description of this surface in its current condition.
helpviewer_keywords: ["GetSurfaceDesc","GetSurfaceDesc method [DirectDraw]","GetSurfaceDesc method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetSurfaceDesc method","IDirectDrawSurface7.GetSurfaceDesc","IDirectDrawSurface7::GetSurfaceDesc","ddraw/IDirectDrawSurface7::GetSurfaceDesc","directdraw.idirectdrawsurface7_getsurfacedesc"]
old-location: directdraw\idirectdrawsurface7_getsurfacedesc.htm
tech.root: directdraw
ms.assetid: 4c36685e-8eb7-4d91-a479-8f099d5e712b
ms.date: 12/05/2018
ms.keywords: GetSurfaceDesc, GetSurfaceDesc method [DirectDraw], GetSurfaceDesc method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetSurfaceDesc method, IDirectDrawSurface7.GetSurfaceDesc, IDirectDrawSurface7::GetSurfaceDesc, ddraw/IDirectDrawSurface7::GetSurfaceDesc, directdraw.idirectdrawsurface7_getsurfacedesc
f1_keywords:
- ddraw/IDirectDrawSurface7.GetSurfaceDesc
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
- IDirectDrawSurface7.GetSurfaceDesc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves a description of this surface in its current condition.

## -parameters

### -param unnamedParam1 [in, out]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that receives the current description of this surface. You need only initialize this structure's <b>dwSize</b> member to the size, in bytes, of the structure prior to the call; no other preparation is required.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>