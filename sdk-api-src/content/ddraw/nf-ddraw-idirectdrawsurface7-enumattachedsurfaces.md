---
UID: NF:ddraw.IDirectDrawSurface7.EnumAttachedSurfaces
title: IDirectDrawSurface7::EnumAttachedSurfaces
author: windows-sdk-content
description: Enumerates all the surfaces that are attached to this surface.
old-location: directdraw\idirectdrawsurface7_enumattachedsurfaces.htm
tech.root: directdraw
ms.assetid: 7f8e9b53-3aff-491c-ab0c-2f414d1ddb27
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumAttachedSurfaces, EnumAttachedSurfaces method [DirectDraw], EnumAttachedSurfaces method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],EnumAttachedSurfaces method, IDirectDrawSurface7.EnumAttachedSurfaces, IDirectDrawSurface7::EnumAttachedSurfaces, ddraw/IDirectDrawSurface7::EnumAttachedSurfaces, directdraw.idirectdrawsurface7_enumattachedsurfaces
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirectDrawSurface7.EnumAttachedSurfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::EnumAttachedSurfaces


## -description


Enumerates all the surfaces that are attached to this surface.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - lpContext [in]

Address of the application-defined structure that is passed to the enumeration member every time that it is called.


#### - lpEnumSurfacesCallback [in]

Address of the <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function to be called for each surface that is attached to this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
</ul>



## -remarks



<b>EnumAttachedSurfaces</b> enumerates only those surfaces that are directly attached to this surface. For example, in a flipping chain of three or more surfaces, only one surface is enumerated because each surface is attached only to the next surface in the flipping chain. In such a configuration, you can call <b>EnumAttachedSurfaces</b> on each successive surface to walk the entire flipping chain.

<b>EnumAttachedSurfaces</b> differs from its counterparts in previous interface versions in that it accepts a pointer to an <a href="https://msdn.microsoft.com/DA0FBED3-B61F-4CC3-9B6D-132A9F8ECFE0">EnumSurfacesCallback7</a> function, rather than an <a href="https://msdn.microsoft.com/4195C266-4F1D-4DD6-935E-78D07ACAA765">EnumSurfacesCallback</a> or <a href="https://msdn.microsoft.com/BC10A26B-50A3-48C5-94D7-B9C9E8FFE768">EnumSurfacesCallback2</a> function.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>EnumAttachedSurfaces</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

