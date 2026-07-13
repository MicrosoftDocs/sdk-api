---
UID: NF:dcomp.IDCompositionSurfaceFactory.CreateVirtualSurface
title: IDCompositionSurfaceFactory::CreateVirtualSurface (dcomp.h)
description: Creates a sparsely populated surface that can be associated with one or more visuals for composition. (IDCompositionSurfaceFactory.CreateVirtualSurface)
helpviewer_keywords: ["CreateVirtualSurface","CreateVirtualSurface method [DirectComposition]","CreateVirtualSurface method [DirectComposition]","IDCompositionSurfaceFactory interface","IDCompositionSurfaceFactory interface [DirectComposition]","CreateVirtualSurface method","IDCompositionSurfaceFactory.CreateVirtualSurface","IDCompositionSurfaceFactory::CreateVirtualSurface","dcomp/IDCompositionSurfaceFactory::CreateVirtualSurface","directcomp.idcompositionsurfacefactory_createvirtualsurface"]
old-location: directcomp\idcompositionsurfacefactory_createvirtualsurface.htm
tech.root: directcomp
ms.assetid: 0C74CDA5-4491-4D16-B972-C9C54007A2FB
ms.date: 12/05/2018
ms.keywords: CreateVirtualSurface, CreateVirtualSurface method [DirectComposition], CreateVirtualSurface method [DirectComposition],IDCompositionSurfaceFactory interface, IDCompositionSurfaceFactory interface [DirectComposition],CreateVirtualSurface method, IDCompositionSurfaceFactory.CreateVirtualSurface, IDCompositionSurfaceFactory::CreateVirtualSurface, dcomp/IDCompositionSurfaceFactory::CreateVirtualSurface, directcomp.idcompositionsurfacefactory_createvirtualsurface
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
 - IDCompositionSurfaceFactory::CreateVirtualSurface
 - dcomp/IDCompositionSurfaceFactory::CreateVirtualSurface
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
 - IDCompositionSurfaceFactory.CreateVirtualSurface
---

# IDCompositionSurfaceFactory::CreateVirtualSurface


## -description

Creates a sparsely populated surface that can be associated with one or more visuals for composition.

## -parameters

### -param initialWidth [in]

The width of the surface, in pixels. The maximum width is 16,777,216 pixels.

### -param initialHeight [in]

The height of the surface, in pixels.
The maximum height is 16,777,216 pixels.

### -param pixelFormat [in]

The pixel format of the surface.

### -param alphaMode [in]

The format of the alpha channel, if an alpha channel is included in the pixel format. This can be one of DXGI_ALPHA_MODE_PREMULTIPLIED or DXGI_ALPHA_MODE_IGNORE. It can also be DXGI_ALPHA_MODE_UNSPECIFIED, which is interpreted as DXGI_ALPHA_MODE_IGNORE.

### -param virtualSurface [out]

The newly created virtual surface object. This parameter must not be NULL.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A newly created virtual surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that is initialized with 100% transparent pixels. 



To initialize the surface with pixel data, use the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionsurface-begindraw">IDCompositionSurface::BeginDraw</a> method. This method not only provides pixels for the surface, but it also allocates actual storage space for those pixels. The memory allocation persists until the application returns some of the memory to the system. The application can free part or all of the allocated memory by calling the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim">IDCompositionVirtualSurface::Trim</a> or <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize">IDCompositionVirtualSurface::Resize</a> method.

Microsoft DirectComposition surfaces support the following pixel formats:


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
