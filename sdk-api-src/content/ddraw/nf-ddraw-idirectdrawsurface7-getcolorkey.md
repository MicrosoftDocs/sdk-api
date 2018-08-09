---
UID: NF:ddraw.IDirectDrawSurface7.GetColorKey
title: IDirectDrawSurface7::GetColorKey
author: windows-sdk-content
description: Retrieves the color key value for this surface.
old-location: directdraw\idirectdrawsurface7_getcolorkey.htm
old-project: directdraw
ms.assetid: 0df14c63-f962-4823-873a-3fe1d626f4cb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DDCKEY_DESTBLT, DDCKEY_DESTOVERLAY, DDCKEY_SRCBLT, DDCKEY_SRCOVERLAY, GetColorKey, GetColorKey method [DirectDraw], GetColorKey method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetColorKey method, IDirectDrawSurface7.GetColorKey, IDirectDrawSurface7::GetColorKey, ddraw/IDirectDrawSurface7::GetColorKey, directdraw.idirectdrawsurface7_getcolorkey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.GetColorKey
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::GetColorKey


## -description


Retrieves the color key value for this surface.


## -parameters




### -param






#### - dwFlags [in]

A value that can be set to one of the following flags to specify the color key to retrieve:



#### DDCKEY_DESTBLT

A color key or color space to be used as a destination color key for bit block transfer (bitblt) operations.



#### DDCKEY_DESTOVERLAY

A color key or color space to be used as a destination color key for overlay operations.



#### DDCKEY_SRCBLT

A color key or color space to be used as a source color key for bitblt operations.



#### DDCKEY_SRCOVERLAY

A color key or color space to be used as a source color key for overlay operations.


#### - lpDDColorKey [out]

A pointer to a <a href="https://msdn.microsoft.com/c520e649-86f9-4c4a-bb67-22d75aa3c8b0">DDCOLORKEY</a> structure that receives the current values for the specified color key of the DirectDrawSurface object.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCOLORKEY</li>
<li>DDERR_NOCOLORKEYHW</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetColorKey</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

