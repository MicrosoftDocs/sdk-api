---
UID: NF:ddraw.IDirectDrawSurface7.GetDC
title: IDirectDrawSurface7::GetDC method
author: windows-driver-content
description: Creates a GDI-compatible handle of a device context for this surface.
old-location: directdraw\idirectdrawsurface7_getdc.htm
old-project: directdraw
ms.assetid: 683be1bc-8232-42de-907f-1136ffdd524d
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetDC method [DirectDraw], GetDC method [DirectDraw], IDirectDrawSurface7 interface, GetDC,IDirectDrawSurface7.GetDC, IDirectDrawSurface7, IDirectDrawSurface7 interface [DirectDraw], GetDC method, IDirectDrawSurface7::GetDC, ddraw/IDirectDrawSurface7::GetDC, directdraw.idirectdrawsurface7_getdc
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDrawSurface7.GetDC
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::GetDC method


## -description


Creates a GDI-compatible handle of a device context for this surface.


## -parameters






#### - lphDC [out]

A pointer to a variable that receives the handle of the device context for this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_DCALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
<li>DDERR_WASSTILLDRAWING</li>
</ul>



## -remarks



<b>GetDC</b> uses an internal version of the <a href="https://msdn.microsoft.com/0267ad70-e7cc-41e8-8325-7ede4a662d13">IDirectDrawSurface7::Lock</a> method to lock the surface. The surface remains locked until the <a href="https://msdn.microsoft.com/170d5194-9327-4632-a87f-39aa8a0ccf74">IDirectDrawSurface7::ReleaseDC</a> method is called.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetDC</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

