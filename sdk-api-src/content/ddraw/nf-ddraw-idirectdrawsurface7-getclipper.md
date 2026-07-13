---
UID: NF:ddraw.IDirectDrawSurface7.GetClipper
title: IDirectDrawSurface7::GetClipper (ddraw.h)
description: Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.
helpviewer_keywords: ["GetClipper","GetClipper method [DirectDraw]","GetClipper method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetClipper method","IDirectDrawSurface7.GetClipper","IDirectDrawSurface7::GetClipper","ddraw/IDirectDrawSurface7::GetClipper","directdraw.idirectdrawsurface7_getclipper"]
old-location: directdraw\idirectdrawsurface7_getclipper.htm
tech.root: directdraw
ms.assetid: f2156dbe-88b5-4ab1-a310-13a38ebdbb4b
ms.date: 12/05/2018
ms.keywords: GetClipper, GetClipper method [DirectDraw], GetClipper method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetClipper method, IDirectDrawSurface7.GetClipper, IDirectDrawSurface7::GetClipper, ddraw/IDirectDrawSurface7::GetClipper, directdraw.idirectdrawsurface7_getclipper
f1_keywords:
- ddraw/IDirectDrawSurface7.GetClipper
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
- IDirectDrawSurface7.GetClipper
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable to receive a pointer to the clipper's <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a> interface.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCLIPPERATTACHED</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>