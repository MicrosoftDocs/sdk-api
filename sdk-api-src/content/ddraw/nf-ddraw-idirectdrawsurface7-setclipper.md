---
UID: NF:ddraw.IDirectDrawSurface7.SetClipper
title: IDirectDrawSurface7::SetClipper (ddraw.h)
description: Attaches a clipper object to, or deletes one from, this surface.
helpviewer_keywords: ["IDirectDrawSurface7 interface [DirectDraw]","SetClipper method","IDirectDrawSurface7.SetClipper","IDirectDrawSurface7::SetClipper","SetClipper","SetClipper method [DirectDraw]","SetClipper method [DirectDraw]","IDirectDrawSurface7 interface","ddraw/IDirectDrawSurface7::SetClipper","directdraw.idirectdrawsurface7_setclipper"]
old-location: directdraw\idirectdrawsurface7_setclipper.htm
tech.root: directdraw
ms.assetid: 18bc8018-b00c-40ef-a54a-e2eecdb835a9
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetClipper method, IDirectDrawSurface7.SetClipper, IDirectDrawSurface7::SetClipper, SetClipper, SetClipper method [DirectDraw], SetClipper method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetClipper, directdraw.idirectdrawsurface7_setclipper
f1_keywords:
- ddraw/IDirectDrawSurface7.SetClipper
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
- IDirectDrawSurface7.SetClipper
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Attaches a clipper object to, or deletes one from, this surface.

## -parameters

### -param unnamedParam1 [in]

A pointer to the <a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawclipper">IDirectDrawClipper</a> interface for the DirectDrawClipper object to be attached to the DirectDrawSurface object. If you set this parameter to NULL, the current DirectDrawClipper object is detached.

## -returns

If the method succeeds, the return value is DD_OK.

If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOCLIPPERATTACHED</li>
</ul>

## -remarks

When you set a clipper to a surface for the first time, <b>SetClipper</b> increments the clipper's reference count; subsequent calls do not affect the clipper's reference count. If you pass NULL as the <i>lpDDClipper</i> parameter, the clipper is removed from the surface, and the clipper's reference count is decremented. If you do not delete the clipper, the surface automatically releases its reference to the clipper when the surface itself is released. According to COM rules, your application must release any references that it holds to the clipper when the object is no longer needed.

<b>SetClipper</b> is primarily used by surfaces that are being overlaid on or bitbltted to the primary surface. However, it can be used on any surface. After a DirectDrawClipper object has been attached and a clip list is associated with it, the DirectDrawClipper object is used for the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a>, <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a>, and <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">IDirectDrawSurface7::UpdateOverlay</a> operations that involve the parent DirectDrawSurface object. <b>SetClipper</b> can also detach the current DirectDrawClipper object of a DirectDrawSurface object.








## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 