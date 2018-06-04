---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirectDrawSurface7::SetSurfaceDesc


## -description


Sets the characteristics of an existing surface.


## -parameters




### -param






#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lpDDsd2 [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550340">DDSURFACEDESC2</a> structure that contains the new surface characteristics.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_INVALIDCAPS</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_GENERIC</li>
</ul>



## -remarks



Currently, you can use <b>SetSurfaceDesc</b> only to set the surface data and pixel format that is used by an explicit system-memory surface. This is useful because it allows a surface to use data from a previously allocated buffer without copying. The new surface memory is allocated by the client application, and therefore the client application must also deallocate it.

The DirectDrawSurface object does not deallocate surface memory that it did not allocate. Therefore, when the surface memory is no longer needed, you must deallocate it. However, when you call <b>SetSurfaceDesc</b>, DirectDraw frees the original surface memory that it implicitly allocated when it created the surface.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetSurfaceDesc</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

