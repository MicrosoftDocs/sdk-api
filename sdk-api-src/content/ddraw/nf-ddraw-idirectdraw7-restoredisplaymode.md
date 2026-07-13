---
UID: NF:ddraw.IDirectDraw7.RestoreDisplayMode
title: IDirectDraw7::RestoreDisplayMode (ddraw.h)
description: Resets the mode of the display device hardware for the primary surface to what it was before the IDirectDraw7::SetDisplayMode method was called. Exclusive-level access is required to use this method.
helpviewer_keywords: ["IDirectDraw7 interface [DirectDraw]","RestoreDisplayMode method","IDirectDraw7.RestoreDisplayMode","IDirectDraw7::RestoreDisplayMode","RestoreDisplayMode","RestoreDisplayMode method [DirectDraw]","RestoreDisplayMode method [DirectDraw]","IDirectDraw7 interface","ddraw/IDirectDraw7::RestoreDisplayMode","directdraw.idirectdraw7_restoredisplaymode"]
old-location: directdraw\idirectdraw7_restoredisplaymode.htm
tech.root: directdraw
ms.assetid: 7538339a-8886-4b40-9779-17c8ebe81446
ms.date: 12/05/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],RestoreDisplayMode method, IDirectDraw7.RestoreDisplayMode, IDirectDraw7::RestoreDisplayMode, RestoreDisplayMode, RestoreDisplayMode method [DirectDraw], RestoreDisplayMode method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::RestoreDisplayMode, directdraw.idirectdraw7_restoredisplaymode
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
 - IDirectDraw7::RestoreDisplayMode
 - ddraw/IDirectDraw7::RestoreDisplayMode
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
 - IDirectDraw7.RestoreDisplayMode
---

# IDirectDraw7::RestoreDisplayMode


## -description

Resets the mode of the display device hardware for the primary surface to what it was before the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-setdisplaymode">IDirectDraw7::SetDisplayMode</a> method was called. Exclusive-level access is required to use this method.



## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_LOCKEDSURFACES</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>
