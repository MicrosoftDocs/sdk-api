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

# IDirectDrawSurface7::Restore


## -description


Restores a surface that has been lost. This occurs when the surface memory that is associated with the DirectDrawSurface object has been freed.


## -parameters






## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_IMPLICITLYCREATED</li>
<li>DDERR_INCOMPATIBLEPRIMARY</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WRONGMODE</li>
</ul>



## -remarks



<b>Restore</b> restores the memory that was allocated for a surface, but does not reload any bitmaps that might have existed in the surface before it was lost.

Surfaces can be lost because the mode of the graphics adapter was changed or because an application received exclusive access to the graphics adapter and freed all surface memory currently allocated on the adapter. When a DirectDrawSurface object loses its surface memory, many methods return DDERR_SURFACELOST and perform no other function. The <b>IDirectDrawSurface7::Restore</b> method reallocates surface memory and reattaches it to the DirectDrawSurface object.

A single call to <b>Restore</b> restores a DirectDrawSurface object's associated implicit surfaces (back buffers, and so on). An attempt to restore an implicitly created surface results in an error. <b>Restore</b> does not work across explicit attachments that were created by using the <a href="https://msdn.microsoft.com/6d42c5ed-7f05-4450-b1f4-cb9ee6efa7d9">IDirectDrawSurface7::AddAttachedSurface</a> method—each of these surfaces must be restored individually.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>Restore</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

