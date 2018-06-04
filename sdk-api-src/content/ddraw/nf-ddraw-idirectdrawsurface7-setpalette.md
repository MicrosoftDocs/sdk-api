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

# IDirectDrawSurface7::SetPalette


## -description


Attaches a palette object to (or detaches one from) a surface. The surface uses this palette for all subsequent operations. The palette change takes place immediately, without regard to refresh timing.


## -parameters






#### - lpDDPalette [in]

A pointer to the <a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a> interface for the palette object to be used with this surface. If NULL, the current palette is detached.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPIXELFORMAT</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOPALETTEATTACHED</li>
<li>DDERR_NOPALETTEHW</li>
<li>DDERR_NOT8BITCOLOR</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



When you call <b>SetPalette</b> to  set a palette to a surface for the first time, <b>SetPalette</b> increments the palette's reference count; subsequent calls to <b>SetPalette</b> do not affect the palette's reference count. If you pass NULL as the <i>lpDDPalette</i> parameter, the palette is removed from the surface, and the palette's reference count is decremented. If you do not delete the palette, the surface automatically releases its reference to the palette when the surface itself is released. According to COM rules, your application must release any references that it holds to the palette when the object is no longer needed.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetPalette</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

