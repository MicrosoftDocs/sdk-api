---
UID: NF:ddraw.IDirectDraw7.DuplicateSurface
title: IDirectDraw7::DuplicateSurface (ddraw.h)
description: Duplicates a DirectDrawSurface object.
helpviewer_keywords: ["DuplicateSurface","DuplicateSurface method [DirectDraw]","DuplicateSurface method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","DuplicateSurface method","IDirectDraw7.DuplicateSurface","IDirectDraw7::DuplicateSurface","ddraw/IDirectDraw7::DuplicateSurface","directdraw.idirectdraw7_duplicatesurface"]
old-location: directdraw\idirectdraw7_duplicatesurface.htm
tech.root: directdraw
ms.assetid: 515219e9-95e9-41fd-9797-d143cd542ef6
ms.date: 12/05/2018
ms.keywords: DuplicateSurface, DuplicateSurface method [DirectDraw], DuplicateSurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],DuplicateSurface method, IDirectDraw7.DuplicateSurface, IDirectDraw7::DuplicateSurface, ddraw/IDirectDraw7::DuplicateSurface, directdraw.idirectdraw7_duplicatesurface
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
 - IDirectDraw7::DuplicateSurface
 - ddraw/IDirectDraw7::DuplicateSurface
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
 - IDirectDraw7.DuplicateSurface
---

# IDirectDraw7::DuplicateSurface


## -description

Duplicates a DirectDrawSurface object.

## -parameters

### -param unnamedParam1 [in]

Address of the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface for the surface to be duplicated.

### -param unnamedParam2 [out]

Address of a variable to contain an <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface pointer for the newly duplicated DirectDrawSurface object.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANTDUPLICATE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

<b>DuplicateSurface</b> creates a new DirectDrawSurface object that points to the same surface memory as an existing DirectDrawSurface object. This duplicate can be used just like the original object. The surface memory is released after the last object referring to it is released. A primary surface, 3-D surface, or implicitly created surface cannot be duplicated.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>