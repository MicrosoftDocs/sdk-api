---
UID: NF:ddraw.IDirectDrawSurface7.GetClipper
title: IDirectDrawSurface7::GetClipper
author: windows-sdk-content
description: Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.
old-location: directdraw\idirectdrawsurface7_getclipper.htm
tech.root: directdraw
ms.assetid: f2156dbe-88b5-4ab1-a310-13a38ebdbb4b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClipper, GetClipper method [DirectDraw], GetClipper method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetClipper method, IDirectDrawSurface7.GetClipper, IDirectDrawSurface7::GetClipper, ddraw/IDirectDrawSurface7::GetClipper, directdraw.idirectdrawsurface7_getclipper
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
 - IDirectDrawSurface7.GetClipper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetClipper


## -description


Retrieves the DirectDrawClipper object that is associated with this surface, and increments the reference count of the returned clipper.


## -parameters






#### - lplpDDClipper [out]

A pointer to a variable to receive a pointer to the clipper's <a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a> interface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCLIPPERATTACHED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetClipper</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

