---
UID: NF:ddraw.IDirectDrawSurface7.AddAttachedSurface
title: IDirectDrawSurface7::AddAttachedSurface (ddraw.h)
description: Attaches the specified z-buffer surface to this surface.
helpviewer_keywords: ["AddAttachedSurface","AddAttachedSurface method [DirectDraw]","AddAttachedSurface method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","AddAttachedSurface method","IDirectDrawSurface7.AddAttachedSurface","IDirectDrawSurface7::AddAttachedSurface","ddraw/IDirectDrawSurface7::AddAttachedSurface","directdraw.idirectdrawsurface7_addattachedsurface"]
old-location: directdraw\idirectdrawsurface7_addattachedsurface.htm
tech.root: directdraw
ms.assetid: 6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9
ms.date: 12/05/2018
ms.keywords: AddAttachedSurface, AddAttachedSurface method [DirectDraw], AddAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],AddAttachedSurface method, IDirectDrawSurface7.AddAttachedSurface, IDirectDrawSurface7::AddAttachedSurface, ddraw/IDirectDrawSurface7::AddAttachedSurface, directdraw.idirectdrawsurface7_addattachedsurface
f1_keywords:
- ddraw/IDirectDrawSurface7.AddAttachedSurface
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
- IDirectDrawSurface7.AddAttachedSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Attaches the specified z-buffer surface to this surface.

## -parameters

### -param unnamedParam1 [in]

Address of the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the surface to be attached.

## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANNOTATTACHSURFACE</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACEALREADYATTACHED</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



<b>AddAttachedSurface</b> increments the reference count of the surface being attached. You can explicitly unattach the surface and decrement its reference count by using the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-deleteattachedsurface">IDirectDrawSurface7::DeleteAttachedSurface</a> method. Unlike complex surfaces that you create with a single call to <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-createsurface">IDirectDraw7::CreateSurface</a>, surfaces attached with this method are not automatically released. The application must release such surfaces.

You can attach only z-buffer surfaces with this method.






## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 