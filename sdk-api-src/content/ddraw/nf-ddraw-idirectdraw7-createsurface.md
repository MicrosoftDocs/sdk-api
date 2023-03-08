---
UID: NF:ddraw.IDirectDraw7.CreateSurface
title: IDirectDraw7::CreateSurface (ddraw.h)
description: Creates a DirectDrawSurface object for this DirectDraw object.
helpviewer_keywords: ["CreateSurface","CreateSurface method [DirectDraw]","CreateSurface method [DirectDraw]","IDirectDraw7 interface","IDirectDraw7 interface [DirectDraw]","CreateSurface method","IDirectDraw7.CreateSurface","IDirectDraw7::CreateSurface","ddraw/IDirectDraw7::CreateSurface","directdraw.idirectdraw7_createsurface"]
old-location: directdraw\idirectdraw7_createsurface.htm
tech.root: directdraw
ms.assetid: 4f27e36f-d04f-43ce-9a3d-64c352c8f8d8
ms.date: 12/05/2018
ms.keywords: CreateSurface, CreateSurface method [DirectDraw], CreateSurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],CreateSurface method, IDirectDraw7.CreateSurface, IDirectDraw7::CreateSurface, ddraw/IDirectDraw7::CreateSurface, directdraw.idirectdraw7_createsurface
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
 - IDirectDraw7::CreateSurface
 - ddraw/IDirectDraw7::CreateSurface
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
 - IDirectDraw7.CreateSurface
---

# IDirectDraw7::CreateSurface


## -description

Creates a DirectDrawSurface object for this DirectDraw object.

## -parameters

### -param unnamedParam1 [in]

Address of a <a href="/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes the requested surface. Set any unused members of the <b>DDSURFACEDESC2</b> structure to 0 before calling this method. A <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure is a member of <b>DDSURFACEDESC2</b>.

### -param unnamedParam2 [out]

Address of a variable to be set to a valid <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface pointer if the call succeeds.

### -param unnamedParam3 [in]

Allows for future compatibility with COM aggregation features. Currently, this method returns an error if this parameter is not NULL.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INCOMPATIBLEPRIMARY</li>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_NOALPHAHW</li>
<li>DDERR_NOCOOPERATIVELEVELSET</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_NOEMULATION</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOFLIPHW</li>
<li>DDERR_NOMIPMAPHW</li>
<li>DDERR_NOOVERLAYHW</li>
<li>DDERR_NOZBUFFERHW</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_OUTOFVIDEOMEMORY</li>
<li>DDERR_PRIMARYSURFACEALREADYEXISTS</li>
<li>DDERR_UNSUPPORTEDMODE</li>
</ul>

## -remarks



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdraw7">IDirectDraw7</a>