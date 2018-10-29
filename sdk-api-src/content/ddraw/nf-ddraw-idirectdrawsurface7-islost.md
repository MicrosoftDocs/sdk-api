---
UID: NF:ddraw.IDirectDrawSurface7.IsLost
title: IDirectDrawSurface7::IsLost
author: windows-sdk-content
description: Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.
old-location: directdraw\idirectdrawsurface7_islost.htm
tech.root: directdraw
ms.assetid: f4654478-ca09-4856-8221-ef5454c23535
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],IsLost method, IDirectDrawSurface7.IsLost, IDirectDrawSurface7::IsLost, IsLost, IsLost method [DirectDraw], IsLost method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::IsLost, directdraw.idirectdrawsurface7_islost
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
 - IDirectDrawSurface7.IsLost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::IsLost


## -description


Determines whether the surface memory that is associated with a DirectDrawSurface object has been freed.


## -parameters






## -returns



If the method succeeds, the return value is DD_OK because the memory has not been freed.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
</ul>
You can use this method to determine when you need to reallocate surface memory. When a DirectDrawSurface object loses its surface memory, most methods return DDERR_SURFACELOST and perform no other action.




## -remarks



Surfaces can lose their memory when the mode of the graphics adapter is changed or when an application receives exclusive access to the graphics adapter and frees all surface memory that is currently allocated on the graphics adapter.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>IsLost</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

