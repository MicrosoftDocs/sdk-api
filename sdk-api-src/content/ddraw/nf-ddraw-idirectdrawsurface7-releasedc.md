---
UID: NF:ddraw.IDirectDrawSurface7.ReleaseDC
title: IDirectDrawSurface7::ReleaseDC (ddraw.h)
description: Releases the handle of a device context that was previously obtained by using the IDirectDrawSurface7::GetDC method.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","ReleaseDC method","IDirectDrawSurface7.ReleaseDC","IDirectDrawSurface7::ReleaseDC","ReleaseDC","ReleaseDC method [DirectDraw]","ReleaseDC method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::ReleaseDC","directdraw.idirectdrawsurface7_releasedc"]
old-location: directdraw\idirectdrawsurface7_releasedc.htm
tech.root: directdraw
ms.assetid: 170d5194-9327-4632-a87f-39aa8a0ccf74
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],ReleaseDC method, IDirectDrawSurface7.ReleaseDC, IDirectDrawSurface7::ReleaseDC, ReleaseDC, ReleaseDC method [DirectDraw], ReleaseDC method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::ReleaseDC, directdraw.idirectdrawsurface7_releasedc
f1_keywords:
- ddraw/IDirectDrawSurface7.ReleaseDC
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
- IDirectDrawSurface7.ReleaseDC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Releases the handle of a device context that was previously obtained by using the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a> method.

## -parameters

### -param unnamedParam1 [in]

The handle of a device context that was previously obtained by <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a>.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>

## -remarks

<b>ReleaseDC</b> also unlocks the surface that was previously locked when the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a> method was called.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>