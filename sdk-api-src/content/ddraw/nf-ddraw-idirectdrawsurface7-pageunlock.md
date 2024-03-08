---
UID: NF:ddraw.IDirectDrawSurface7.PageUnlock
title: IDirectDrawSurface7::PageUnlock (ddraw.h)
description: Unlocks a system-memory surface, which then allows it to be paged out.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","PageUnlock method","IDirectDrawSurface7.PageUnlock","IDirectDrawSurface7::PageUnlock","PageUnlock","PageUnlock method [DirectDraw]","PageUnlock method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::PageUnlock","directdraw.idirectdrawsurface7_pageunlock"]
old-location: directdraw\idirectdrawsurface7_pageunlock.htm
tech.root: directdraw
ms.assetid: 1a87df37-a53f-4240-a5cb-47b13999c34b
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],PageUnlock method, IDirectDrawSurface7.PageUnlock, IDirectDrawSurface7::PageUnlock, PageUnlock, PageUnlock method [DirectDraw], PageUnlock method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::PageUnlock, directdraw.idirectdrawsurface7_pageunlock
f1_keywords:
- ddraw/IDirectDrawSurface7.PageUnlock
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
- IDirectDrawSurface7.PageUnlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Unlocks a system-memory surface, which then allows it to be paged out.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANTPAGEUNLOCK</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTPAGELOCKED</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

A lock count is maintained for each surface and is incremented each time that <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pagelock">IDirectDrawSurface7::PageLock</a> is called for that surface. The count is decremented when <b>PageUnlock</b> is called. When the count reaches 0, the memory is unlocked, and can then be paged by the operating system.

<b>PageUnlock</b> works only on system-memory surfaces; it does not page-unlock a display-memory surface or an emulated primary surface. If an application calls <b>PageUnlock</b> on a display memory surface, the method does nothing except return DD_OK.

<b>IDirectDrawSurface7::PageUnlock</b> was not implemented in the <b>IDirectDraw</b> interface version.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>