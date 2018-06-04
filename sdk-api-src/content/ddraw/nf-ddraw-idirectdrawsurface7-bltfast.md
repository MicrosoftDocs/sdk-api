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

# IDirectDrawSurface7::BltFast


## -description


Performs a source copy bitblt or transparent bitblt by using a source color key or destination color key.


## -parameters




### -param






#### - dwFlags [in]

Type of transfer. The following transfers are defined:



#### DDBLTFAST_DESTCOLORKEY

A transparent bitblt that uses the destination color key.



#### DDBLTFAST_NOCOLORKEY

A normal copy bitblt with no transparency.



#### DDBLTFAST_SRCCOLORKEY

A transparent bitblt that uses the source color key.



#### DDBLTFAST_WAIT

Postpones the DDERR_WASSTILLDRAWING message if the bitbltter is busy, and returns as soon as the bitblt can be set up or another error occurs.


#### - dwX [in]

The x-coordinate to bitblt to on the destination surface.


#### - dwY [in]

The y-coordinate to bitblt to on the destination surface.


#### - lpDDBltFx [in]

A pointer to the <a href="https://msdn.microsoft.com/a542434f-61d3-4c73-a087-ffb83a509c67">DDBLTFX</a> structure for the bitblt.


#### - lpDDSrcSurface [in]

A pointer to the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the DirectDrawSurface object that is the source of the bitblt.


#### - lpSrcRect [in]

A pointer to a <b>RECT</b> structure that defines the upper-left and lower-right points of the rectangle to bitblt from on the source surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCEPTION</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



<b>BltFast</b> always attempts an asynchronous blit if it is supported by the hardware.

<b>BltFast</b> works only on display memory surfaces and cannot clip when it performs a bitblt operation. If you use this method on a surface with an attached clipper, the call fails, and the method returns DDERR_UNSUPPORTED.

The software implementation of <b>IDirectDrawSurface7::BltFast</b> is 10 percent faster than the <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a> method. However, there is no speed difference between the two if display hardware is used.

Typically, <b>IDirectDrawSurface7::BltFast</b> returns immediately with an error if the bitbltter is busy and the bitblt cannot be set up. You can use the DDBLTFAST_WAIT flag, however, if you want this method not to return until either the bitblt can be set up or another error occurs.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>BltFast</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

