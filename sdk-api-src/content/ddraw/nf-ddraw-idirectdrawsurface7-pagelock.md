---
UID: NF:ddraw.IDirectDrawSurface7.PageLock
title: IDirectDrawSurface7::PageLock (ddraw.h)
description: Prevents a system-memory surface from being paged out while a bit block transfer (bitblt) operation that uses direct memory access (DMA) transfers to or from system memory is in progress.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","PageLock method","IDirectDrawSurface7.PageLock","IDirectDrawSurface7::PageLock","PageLock","PageLock method [DirectDraw]","PageLock method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::PageLock","directdraw.idirectdrawsurface7_pagelock"]
old-location: directdraw\idirectdrawsurface7_pagelock.htm
tech.root: directdraw
ms.assetid: 018e6539-bb2a-472c-bab4-2c0665cdbe15
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],PageLock method, IDirectDrawSurface7.PageLock, IDirectDrawSurface7::PageLock, PageLock, PageLock method [DirectDraw], PageLock method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::PageLock, directdraw.idirectdrawsurface7_pagelock
f1_keywords:
- ddraw/IDirectDrawSurface7.PageLock
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
- IDirectDrawSurface7.PageLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Prevents a system-memory surface from being paged out while a bit block transfer (bitblt) operation that uses direct memory access (DMA) transfers to or from system memory is in progress.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANTPAGELOCK</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

You must call <b>PageLock</b> to make use of DMA support. If you do not, the bitblt occurs by using software emulation.

The performance of the operating system can be negatively affected if too much memory is locked.

A lock count is maintained for each surface and is incremented each time that <b>PageLock</b> is called for that surface. The count is decremented when <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-pageunlock">IDirectDrawSurface7::PageUnlock</a> is called. When the count reaches 0, the memory is unlocked, and can then be paged by the operating system.

<b>PageLock</b> works only on system-memory surfaces; it does not page-lock a display-memory surface or an emulated primary surface. If an application calls <b>PageLock</b> on a display memory surface, the method does nothing except return DD_OK.

<b>IDirectDrawSurface7::PageLock</b> was not implemented in the <b>IDirectDraw</b> interface version.






## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 