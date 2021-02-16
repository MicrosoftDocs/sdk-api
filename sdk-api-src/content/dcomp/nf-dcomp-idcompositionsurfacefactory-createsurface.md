---
UID: NF:dcomp.IDCompositionSurfaceFactory.CreateSurface
title: IDCompositionSurfaceFactory::CreateSurface (dcomp.h)
description: Creates a surface object that can be associated with one or more visuals for composition.
helpviewer_keywords: ["CreateSurface","CreateSurface method [DirectComposition]","CreateSurface method [DirectComposition]","IDCompositionSurfaceFactory interface","IDCompositionSurfaceFactory interface [DirectComposition]","CreateSurface method","IDCompositionSurfaceFactory.CreateSurface","IDCompositionSurfaceFactory::CreateSurface","dcomp/IDCompositionSurfaceFactory::CreateSurface","directcomp.idcompositionsurfacefactory_createsurface"]
old-location: directcomp\idcompositionsurfacefactory_createsurface.htm
tech.root: directcomp
ms.assetid: C65CD072-C00E-409B-B508-C12CE4ACE73F
ms.date: 12/05/2018
ms.keywords: CreateSurface, CreateSurface method [DirectComposition], CreateSurface method [DirectComposition],IDCompositionSurfaceFactory interface, IDCompositionSurfaceFactory interface [DirectComposition],CreateSurface method, IDCompositionSurfaceFactory.CreateSurface, IDCompositionSurfaceFactory::CreateSurface, dcomp/IDCompositionSurfaceFactory::CreateSurface, directcomp.idcompositionsurfacefactory_createsurface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionSurfaceFactory::CreateSurface
 - dcomp/IDCompositionSurfaceFactory::CreateSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurfaceFactory.CreateSurface
---

# IDCompositionSurfaceFactory::CreateSurface


## -description

Creates a surface object that can be associated with one or more visuals for composition.

## -parameters

### -param width [in]

The width of the surface, in pixels.

### -param height [in]

The height of the surface, in pixels.

### -param pixelFormat [in]

The pixel format of the surface.

### -param alphaMode [in]

The format of the alpha channel, if an alpha channel is included in the pixel format. This can be one of DXGI_ALPHA_MODE_PREMULTIPLIED or DXGI_ALPHA_MODE_IGNORE. It can also be DXGI_ALPHA_MODE_UNSPECIFIED, which is interpreted as DXGI_ALPHA_MODE_IGNORE.

### -param surface [out]

The newly created surface object. This parameter must not be NULL.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A Microsoft DirectComposition surface is a rectangular array of pixels that can be associated with a visual for composition. 

A newly created surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that has 100% transparent pixels. 



To initialize the surface with pixel data, use the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method. The first call to this method must cover the entire surface area to provide an initial value for every pixel. Subsequent calls may specify smaller sub-rectangles of the surface to update.



This method will fail if either the width or height exceed the max texture size. If your scenario requires dimensions beyond the max texture size, use <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurfacefactory-createvirtualsurface">CreateVirtualSurface</a> method.

DirectComposition surfaces support the following pixel formats:


<ul>
<li>DXGI_FORMAT_B8G8R8A8_UNORM
</li>
<li>DXGI_FORMAT_R8G8B8A8_UNORM
	</li>
<li>DXGI_FORMAT_R16G16B16A16_FLOAT</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createsurface">IDCompositionDevice2::CreateSurface</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createvirtualsurface">IDCompositionDevice2::CreateVirtualSurface</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsurfacefactory">IDCompositionSurfaceFactory</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurfacefactory-createvirtualsurface">IDCompositionSurfaceFactory::CreateVirtualSurface</a>