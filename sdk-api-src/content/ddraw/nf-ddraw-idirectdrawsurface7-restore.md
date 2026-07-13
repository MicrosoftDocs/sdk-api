---
UID: NF:ddraw.IDirectDrawSurface7.Restore
title: IDirectDrawSurface7::Restore (ddraw.h)
description: Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","Restore method","IDirectDrawSurface7.Restore","IDirectDrawSurface7::Restore","Restore","Restore method [DirectDraw]","Restore method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::Restore","directdraw.idirectdrawsurface7_restore"]
old-location: directdraw\idirectdrawsurface7_restore.htm
tech.root: directdraw
ms.assetid: 9ca7abb2-5b9a-4323-9f0b-952e183e794b
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],Restore method, IDirectDrawSurface7.Restore, IDirectDrawSurface7::Restore, Restore, Restore method [DirectDraw], Restore method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Restore, directdraw.idirectdrawsurface7_restore
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
 - IDirectDrawSurface7::Restore
 - ddraw/IDirectDrawSurface7::Restore
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
 - IDirectDrawSurface7.Restore
---

# IDirectDrawSurface7::Restore


## -description

Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed.



## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_IMPLICITLYCREATED</li>
<li>DDERR_INCOMPATIBLEPRIMARY</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WRONGMODE</li>
</ul>

## -remarks

<b>Restore</b> restores the memory that was allocated for a surface, but does not reload any bitmaps that might have existed in the surface before it was lost.

Surfaces can be lost because the mode of the graphics adapter was changed or because an application received exclusive access to the graphics adapter and freed all surface memory currently allocated on the adapter. When a DirectDrawSurface object loses its surface memory, many methods return DDERR_SURFACELOST and perform no other function. The <b>IDirectDrawSurface7::Restore</b> method reallocates surface memory and reattaches it to the DirectDrawSurface object.

A single call to <b>Restore</b> restores a DirectDrawSurface object's associated implicit surfaces (back buffers, and so on). An attempt to restore an implicitly created surface results in an error. <b>Restore</b> does not work across explicit attachments that were created by using the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addattachedsurface">IDirectDrawSurface7::AddAttachedSurface</a> method—each of these surfaces must be restored individually.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
