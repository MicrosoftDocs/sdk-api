---
UID: NF:ddraw.IDirectDrawSurface7.GetAttachedSurface
title: IDirectDrawSurface7::GetAttachedSurface (ddraw.h)
description: Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.
helpviewer_keywords: ["GetAttachedSurface","GetAttachedSurface method [DirectDraw]","GetAttachedSurface method [DirectDraw]","IDirectDrawSurface7 interface","IDirectDrawSurface7 interface [DirectDraw]","GetAttachedSurface method","IDirectDrawSurface7.GetAttachedSurface","IDirectDrawSurface7::GetAttachedSurface","ddraw/IDirectDrawSurface7::GetAttachedSurface","directdraw.idirectdrawsurface7_getattachedsurface"]
old-location: directdraw\idirectdrawsurface7_getattachedsurface.htm
tech.root: directdraw
ms.assetid: 0eae7e55-5ff7-41f6-ac6a-ce7fb6d809b9
ms.date: 12/05/2018
ms.keywords: GetAttachedSurface, GetAttachedSurface method [DirectDraw], GetAttachedSurface method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetAttachedSurface method, IDirectDrawSurface7.GetAttachedSurface, IDirectDrawSurface7::GetAttachedSurface, ddraw/IDirectDrawSurface7::GetAttachedSurface, directdraw.idirectdrawsurface7_getattachedsurface
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
 - IDirectDrawSurface7::GetAttachedSurface
 - ddraw/IDirectDrawSurface7::GetAttachedSurface
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
 - IDirectDrawSurface7.GetAttachedSurface
---

# IDirectDrawSurface7::GetAttachedSurface


## -description

Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.

## -parameters

### -param unnamedParam1 [in]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure that indicates the hardware capabilities of the attached surface.

### -param unnamedParam2 [out]

A pointer to a variable to receive a pointer to the retrieved surface's <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a> interface. The retrieved surface is the one that matches the description, according to the <i>lpDDSCaps</i> parameter.

## -returns

If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
<li>DDERR_SURFACELOST</li>
</ul>

## -remarks

Attachments are used to connect multiple DirectDrawSurface objects into complex structures, like the complex structures required to support 3-D page flipping with z-buffers. <b>GetAttachedSurface</b> fails if more than one surface is attached that matches the capabilities requested. In this case, the application must use the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-enumattachedsurfaces">IDirectDrawSurface7::EnumAttachedSurfaces</a> method to obtain the attached surfaces.





## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>