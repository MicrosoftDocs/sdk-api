---
UID: NF:ddraw.IDirectDraw7.CreateClipper
title: IDirectDraw7::CreateClipper (ddraw.h)
description: Creates a DirectDrawClipper object.
helpviewer_keywords: ["CreateClipper","CreateClipper method [DirectDraw]","CreateClipper method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","CreateClipper method","IDirectDraw7.CreateClipper","IDirectDraw7::CreateClipper","ddraw/IDirectDraw7::CreateClipper","directdraw.idirectdraw7_createclipper"]
old-location: directdraw\idirectdraw7_createclipper.htm
tech.root: directdraw
ms.assetid: 123a07c0-d371-4d10-bff8-b5640bd3b920
ms.date: 12/05/2018
ms.keywords: CreateClipper, CreateClipper method [DirectDraw], CreateClipper method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],CreateClipper method, IDirectDraw7.CreateClipper, IDirectDraw7::CreateClipper, ddraw/IDirectDraw7::CreateClipper, directdraw.idirectdraw7_createclipper
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
 - IDirectDraw7::CreateClipper
 - ddraw/IDirectDraw7::CreateClipper
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
 - IDirectDraw7.CreateClipper
---

# IDirectDraw7::CreateClipper


## -description

Creates a DirectDrawClipper object.

## -parameters

### -param unnamedParam1 [in]

Currently not used and must be set to 0.

### -param unnamedParam2 [out]

Address of a variable to be set to a valid <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a> interface pointer if the call succeeds.

### -param unnamedParam3 [in]

Allows for future compatibility with COM aggregation features. Currently this method returns an error if this parameter is not NULL.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCOOPERATIVELEVELSET</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>

## -remarks

The DirectDrawClipper object can be attached to a DirectDrawSurface and used during <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a>, and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">IDirectDrawSurface7::UpdateOverlay</a> operations.

To create a DirectDrawClipper object that is not owned by a specific DirectDraw object, use the <a href="/windows/desktop/api/ddraw/nf-ddraw-directdrawcreateclipper">DirectDrawCreateClipper</a> function.



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>