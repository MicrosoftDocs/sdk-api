---
UID: NF:ddraw.IDirectDrawSurface7.Unlock
title: IDirectDrawSurface7::Unlock (ddraw.h)
description: Notifies DirectDraw that the direct surface manipulations are complete.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","Unlock method","IDirectDrawSurface7.Unlock","IDirectDrawSurface7::Unlock","Unlock","Unlock method [DirectDraw]","Unlock method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::Unlock","directdraw.idirectdrawsurface7_unlock"]
old-location: directdraw\idirectdrawsurface7_unlock.htm
tech.root: directdraw
ms.assetid: 1606869a-83b1-4278-a0b5-c183cc7ea285
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],Unlock method, IDirectDrawSurface7.Unlock, IDirectDrawSurface7::Unlock, Unlock, Unlock method [DirectDraw], Unlock method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Unlock, directdraw.idirectdrawsurface7_unlock
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
 - IDirectDrawSurface7::Unlock
 - ddraw/IDirectDrawSurface7::Unlock
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
 - IDirectDrawSurface7.Unlock
---

## -description

Notifies DirectDraw that the direct surface manipulations are complete.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <b>RECT</b> structure that was used to lock the surface in the corresponding call to the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">IDirectDrawSurface7::Lock</a> method. This parameter can be NULL only if the entire surface was locked by passing NULL in the <i>lpDestRect</i> parameter of the corresponding call to the <b>IDirectDrawSurface7::Lock</b> method.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOTLOCKED</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

Because you can call <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-lock">IDirectDrawSurface7::Lock</a> multiple times for the same surface with different destination rectangles, the pointer in <i>lpRect</i> links the calls to the <b>IDirectDrawSurface7::Lock</b> and <b>IDirectDrawSurface7::Unlock</b> methods.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>