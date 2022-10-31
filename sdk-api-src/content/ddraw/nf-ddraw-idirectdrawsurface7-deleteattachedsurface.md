---
UID: NF:ddraw.IDirectDrawSurface7.DeleteAttachedSurface
title: IDirectDrawSurface7::DeleteAttachedSurface (ddraw.h)
description: Detaches one or more attached surfaces.
helpviewer_keywords: ["DeleteAttachedSurface","DeleteAttachedSurface method [DirectDraw]","DeleteAttachedSurface method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","DeleteAttachedSurface method","IDirectDrawSurface7.DeleteAttachedSurface","IDirectDrawSurface7::DeleteAttachedSurface","ddraw/IDirectDrawSurface7::DeleteAttachedSurface","directdraw.idirectdrawsurface7_deleteattachedsurface"]
old-location: directdraw\idirectdrawsurface7_deleteattachedsurface.htm
tech.root: directdraw
ms.assetid: 39cefecd-2ae0-42ba-8140-842acdaa1ad8
ms.date: 12/05/2018
ms.keywords: DeleteAttachedSurface, DeleteAttachedSurface method [DirectDraw], DeleteAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],DeleteAttachedSurface method, IDirectDrawSurface7.DeleteAttachedSurface, IDirectDrawSurface7::DeleteAttachedSurface, ddraw/IDirectDrawSurface7::DeleteAttachedSurface, directdraw.idirectdrawsurface7_deleteattachedsurface
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
 - IDirectDrawSurface7::DeleteAttachedSurface
 - ddraw/IDirectDrawSurface7::DeleteAttachedSurface
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
 - IDirectDrawSurface7.DeleteAttachedSurface
---

# IDirectDrawSurface7::DeleteAttachedSurface


## -description

Detaches one or more attached surfaces.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

### -param unnamedParam2 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the DirectDrawSurface object to be detached. If this parameter is NULL, all attached surfaces become detached.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANNOTDETACHSURFACE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_SURFACENOTATTACHED</li>
</ul>

## -remarks

<b>DeleteAttachedSurface</b> decrements the reference count of the surface to be detached. If the reference count of the surface to be detached reaches 0, the surface is lost and removed from memory.

Implicit attachments, those formed by DirectDraw rather than the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-addattachedsurface">IDirectDrawSurface7::AddAttachedSurface</a> method, cannot be detached. Detaching surfaces from a flipping chain can alter other surfaces in the chain. If a front buffer is detached from a flipping chain, the next surface in the chain becomes the front buffer, and the following surface becomes the back buffer. If a back buffer is detached from a chain, the following surface becomes a back buffer. If a plain surface is detached from a chain, the chain simply becomes shorter. If a flipping chain has only two surfaces and they are detached, the chain is destroyed, and both surfaces return to their previous designations.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>