---
UID: NF:ddraw.IDirectDrawSurface7.ChangeUniquenessValue
title: IDirectDrawSurface7::ChangeUniquenessValue (ddraw.h)
description: Manually updates the uniqueness value for this surface.
helpviewer_keywords: ["ChangeUniquenessValue","ChangeUniquenessValue method [DirectDraw]","ChangeUniquenessValue method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","ChangeUniquenessValue method","IDirectDrawSurface7.ChangeUniquenessValue","IDirectDrawSurface7::ChangeUniquenessValue","ddraw/IDirectDrawSurface7::ChangeUniquenessValue","directdraw.idirectdrawsurface7_changeuniquenessvalue"]
old-location: directdraw\idirectdrawsurface7_changeuniquenessvalue.htm
tech.root: directdraw
ms.assetid: 4d714fb7-7e12-45ab-ae40-7fc2a65b9e7e
ms.date: 12/05/2018
ms.keywords: ChangeUniquenessValue, ChangeUniquenessValue method [DirectDraw], ChangeUniquenessValue method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],ChangeUniquenessValue method, IDirectDrawSurface7.ChangeUniquenessValue, IDirectDrawSurface7::ChangeUniquenessValue, ddraw/IDirectDrawSurface7::ChangeUniquenessValue, directdraw.idirectdrawsurface7_changeuniquenessvalue
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
 - IDirectDrawSurface7::ChangeUniquenessValue
 - ddraw/IDirectDrawSurface7::ChangeUniquenessValue
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
 - IDirectDrawSurface7.ChangeUniquenessValue
---

# IDirectDrawSurface7::ChangeUniquenessValue


## -description

Manually updates the uniqueness value for this surface.



## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>

## -remarks

DirectDraw automatically updates uniqueness values whenever the contents of a surface change.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
