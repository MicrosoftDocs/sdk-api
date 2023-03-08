---
UID: NF:ddraw.IDirectDrawSurface7.GetUniquenessValue
title: IDirectDrawSurface7::GetUniquenessValue (ddraw.h)
description: Retrieves the current uniqueness value for this surface.
helpviewer_keywords: ["GetUniquenessValue","GetUniquenessValue method [DirectDraw]","GetUniquenessValue method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetUniquenessValue method","IDirectDrawSurface7.GetUniquenessValue","IDirectDrawSurface7::GetUniquenessValue","ddraw/IDirectDrawSurface7::GetUniquenessValue","directdraw.idirectdrawsurface7_getuniquenessvalue"]
old-location: directdraw\idirectdrawsurface7_getuniquenessvalue.htm
tech.root: directdraw
ms.assetid: 559d9381-1135-47de-9bbe-49aa8d97f5d3
ms.date: 12/05/2018
ms.keywords: GetUniquenessValue, GetUniquenessValue method [DirectDraw], GetUniquenessValue method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetUniquenessValue method, IDirectDrawSurface7.GetUniquenessValue, IDirectDrawSurface7::GetUniquenessValue, ddraw/IDirectDrawSurface7::GetUniquenessValue, directdraw.idirectdrawsurface7_getuniquenessvalue
f1_keywords:
- ddraw/IDirectDrawSurface7.GetUniquenessValue
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
- IDirectDrawSurface7.GetUniquenessValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the current uniqueness value for this surface.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives the surface's current uniqueness value if the call succeeds.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

The only defined uniqueness value is 0, which indicates that the surface is likely to be changing beyond the control of DirectDraw. Other uniqueness values are significant only if they differ from a previously cached uniqueness value. If the current value is different from a cached value, the contents of the surface have changed.






## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 