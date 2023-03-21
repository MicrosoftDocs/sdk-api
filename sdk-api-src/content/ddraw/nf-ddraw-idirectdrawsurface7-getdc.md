---
UID: NF:ddraw.IDirectDrawSurface7.GetDC
title: IDirectDrawSurface7::GetDC (ddraw.h)
description: Creates a GDI-compatible handle of a device context for this surface.
helpviewer_keywords: ["GetDC","GetDC method [DirectDraw]","GetDC method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetDC method","IDirectDrawSurface7.GetDC","IDirectDrawSurface7::GetDC","ddraw/IDirectDrawSurface7::GetDC","directdraw.idirectdrawsurface7_getdc"]
old-location: directdraw\idirectdrawsurface7_getdc.htm
tech.root: directdraw
ms.assetid: 683be1bc-8232-42de-907f-1136ffdd524d
ms.date: 12/05/2018
ms.keywords: GetDC, GetDC method [DirectDraw], GetDC method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetDC method, IDirectDrawSurface7.GetDC, IDirectDrawSurface7::GetDC, ddraw/IDirectDrawSurface7::GetDC, directdraw.idirectdrawsurface7_getdc
f1_keywords:
- ddraw/IDirectDrawSurface7.GetDC
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
- IDirectDrawSurface7.GetDC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Creates a GDI-compatible handle of a device context for this surface.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the handle of the device context for this surface.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_DCALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



<b>GetDC</b> uses an internal version of the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">IDirectDrawSurface7::Lock</a> method to lock the surface. The surface remains locked until the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-releasedc">IDirectDrawSurface7::ReleaseDC</a> method is called.






## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 