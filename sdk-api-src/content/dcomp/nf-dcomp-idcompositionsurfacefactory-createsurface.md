---
UID: NF:dcomp.IDCompositionSurfaceFactory.CreateSurface
title: IDCompositionSurfaceFactory::CreateSurface
author: windows-sdk-content
description: Creates a surface object that can be associated with one or more visuals for composition.
old-location: directcomp\idcompositionsurfacefactory_createsurface.htm
tech.root: directcomp
ms.assetid: C65CD072-C00E-409B-B508-C12CE4ACE73F
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateSurface, CreateSurface method [DirectComposition], CreateSurface method [DirectComposition],IDCompositionSurfaceFactory interface, IDCompositionSurfaceFactory interface [DirectComposition],CreateSurface method, IDCompositionSurfaceFactory.CreateSurface, IDCompositionSurfaceFactory::CreateSurface, dcomp/IDCompositionSurfaceFactory::CreateSurface, directcomp.idcompositionsurfacefactory_createsurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionSurfaceFactory.CreateSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A Microsoft DirectComposition surface is a rectangular array of pixels that can be associated with a visual for composition. 

A newly created surface object is in an uninitialized state. While it is uninitialized, the surface has no effect on the composition of the visual tree. It behaves exactly like a surface that has 100% transparent pixels. 



To initialize the surface with pixel data, use the <a href="https://msdn.microsoft.com/0D7E90A1-90E4-44BE-A4DA-8DA300C81A35">IDCompositionSurface::BeginDraw</a> method. The first call to this method must cover the entire surface area to provide an initial value for every pixel. Subsequent calls may specify smaller sub-rectangles of the surface to update.



This method will fail if either the width or height exceed the max texture size. If your scenario requires dimensions beyond the max texture size, use <a href="https://msdn.microsoft.com/0C74CDA5-4491-4D16-B972-C9C54007A2FB">CreateVirtualSurface</a> method.

DirectComposition surfaces support the following pixel formats:


<ul>
<li>DXGI_FORMAT_B8G8R8A8_UNORM
</li>
<li>DXGI_FORMAT_R8G8B8A8_UNORM
	</li>
<li>DXGI_FORMAT_R16G16B16A16_FLOAT</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1CBE92B6-AC48-47F1-B50A-B78030D356D8">IDCompositionDevice2::CreateSurface</a>



<a href="https://msdn.microsoft.com/659D79E3-2E7C-4431-B724-7AC2978BD9BC">IDCompositionDevice2::CreateVirtualSurface</a>



<a href="https://msdn.microsoft.com/1BB028E0-376E-42BD-82FD-08331341C93B">IDCompositionSurfaceFactory</a>



<a href="https://msdn.microsoft.com/0C74CDA5-4491-4D16-B972-C9C54007A2FB">IDCompositionSurfaceFactory::CreateVirtualSurface</a>
 

 

