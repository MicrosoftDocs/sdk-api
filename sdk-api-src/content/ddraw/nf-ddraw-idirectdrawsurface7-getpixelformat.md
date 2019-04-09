---
UID: NF:ddraw.IDirectDrawSurface7.GetPixelFormat
title: IDirectDrawSurface7::GetPixelFormat (ddraw.h)
author: windows-sdk-content
description: Retrieves the color and pixel format of this surface.
old-location: directdraw\idirectdrawsurface7_getpixelformat.htm
tech.root: directdraw
ms.assetid: 2c33c46b-6cd7-4ee7-976c-a81f9d92b379
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [DirectDraw], GetPixelFormat method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPixelFormat method, IDirectDrawSurface7.GetPixelFormat, IDirectDrawSurface7::GetPixelFormat, ddraw/IDirectDrawSurface7::GetPixelFormat, directdraw.idirectdrawsurface7_getpixelformat
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
 - IDirectDrawSurface7.GetPixelFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetPixelFormat


## -description


Retrieves the color and pixel format of this surface.


## -parameters






#### - lpDDPixelFormat [out]

A pointer to a <a href="https://msdn.microsoft.com/17c531cb-7e65-482a-b3de-494874c1dd92">DDPIXELFORMAT</a> structure that receives a detailed description of the current pixel and color space format of this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetPixelFormat</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

