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

# IDirectDrawSurface7::GetAttachedSurface


## -description


Obtains the attached surface that has the specified capabilities, and increments the reference count of the retrieved interface.


## -parameters




### -param






#### - lpDDSCaps [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure that indicates the hardware capabilities of the attached surface.


#### - lplpDDAttachedSurface [out]

A pointer to a variable to receive a pointer to the retrieved surface's <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface. The retrieved surface is the one that matches the description, according to the <i>lpDDSCaps</i> parameter.


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



Attachments are used to connect multiple DirectDrawSurface objects into complex structures, like the complex structures required to support 3-D page flipping with z-buffers. <b>GetAttachedSurface</b> fails if more than one surface is attached that matches the capabilities requested. In this case, the application must use the <a href="https://msdn.microsoft.com/7f8e9b53-3aff-491c-ab0c-2f414d1ddb27">IDirectDrawSurface7::EnumAttachedSurfaces</a> method to obtain the attached surfaces.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetAttachedSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

