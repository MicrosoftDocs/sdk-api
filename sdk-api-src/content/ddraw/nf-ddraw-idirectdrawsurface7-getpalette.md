---
UID: NF:ddraw.IDirectDrawSurface7.GetPalette
title: IDirectDrawSurface7::GetPalette
author: windows-sdk-content
description: Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.
old-location: directdraw\idirectdrawsurface7_getpalette.htm
tech.root: directdraw
ms.assetid: 35a667aa-9a69-4c71-9e26-b42359815a0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPalette, GetPalette method [DirectDraw], GetPalette method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetPalette method, IDirectDrawSurface7.GetPalette, IDirectDrawSurface7::GetPalette, ddraw/IDirectDrawSurface7::GetPalette, directdraw.idirectdrawsurface7_getpalette
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
 - IDirectDrawSurface7.GetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetPalette


## -description


Retrieves the DirectDrawPalette object that is associated with this surface, and increments the reference count of the returned palette.


## -parameters






#### - lplpDDPalette [out]

A pointer to a variable to receive a pointer to the palette object's <a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a> interface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOEXCLUSIVEMODE</li>
<li>DDERR_NOPALETTEATTACHED</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetPalette</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

