---
UID: NF:ddraw.IDirectDrawSurface7.SetColorKey
title: IDirectDrawSurface7::SetColorKey
author: windows-sdk-content
description: Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.
old-location: directdraw\idirectdrawsurface7_setcolorkey.htm
tech.root: directdraw
ms.assetid: 36f2510e-d12a-40af-b65c-aa36ce46a942
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DDCKEY_COLORSPACE, DDCKEY_DESTBLT, DDCKEY_DESTOVERLAY, DDCKEY_SRCBLT, DDCKEY_SRCOVERLAY, IDirectDrawSurface7 interface [DirectDraw],SetColorKey method, IDirectDrawSurface7.SetColorKey, IDirectDrawSurface7::SetColorKey, SetColorKey, SetColorKey method [DirectDraw], SetColorKey method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetColorKey, directdraw.idirectdrawsurface7_setcolorkey
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
 - IDirectDrawSurface7.SetColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::SetColorKey


## -description


Sets the color key value for the DirectDrawSurface object if the hardware supports color keys on a per-surface basis.


## -parameters




### -param arg1 [in]

A value that can be set to one of the following flags to specify the requested color key:



#### DDCKEY_COLORSPACE

The structure contains a color space. Not set if the structure contains a single color key.



#### DDCKEY_DESTBLT

A color key or color space to be used as a destination color key for bit block transfer (bitblt) operations.



#### DDCKEY_DESTOVERLAY

A color key or color space to be used as a destination color key for overlay operations.



#### DDCKEY_SRCBLT

A color key or color space to be used as a source color key for bitblt operations.



#### DDCKEY_SRCOVERLAY

A color key or color space to be used as a source color key for overlay operations.


### -param arg2 [in]

A pointer to a <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that contains the new color key values for the DirectDrawSurface object. This value can be NULL to remove a previously set color key.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOOVERLAYHW</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



For transparent bitblt operations and overlays, set destination color on the destination surface and source color on the source surface.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetColorKey</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

