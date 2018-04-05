---
UID: NF:ddraw.IDirectDrawSurface7.ReleaseDC
title: IDirectDrawSurface7::ReleaseDC method
author: windows-driver-content
description: Releases the handle of a device context that was previously obtained by using the IDirectDrawSurface7::GetDC method.
old-location: directdraw\idirectdrawsurface7_releasedc.htm
old-project: directdraw
ms.assetid: 170d5194-9327-4632-a87f-39aa8a0ccf74
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDirectDrawSurface7, IDirectDrawSurface7 interface [DirectDraw], ReleaseDC method, IDirectDrawSurface7::ReleaseDC, ReleaseDC method [DirectDraw], ReleaseDC method [DirectDraw], IDirectDrawSurface7 interface, ReleaseDC,IDirectDrawSurface7.ReleaseDC, ddraw/IDirectDrawSurface7::ReleaseDC, directdraw.idirectdrawsurface7_releasedc
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
-	IDirectDrawSurface7.ReleaseDC
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::ReleaseDC method


## -description


Releases the handle of a device context that was previously obtained by using the <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a> method.



## -parameters






#### - hDC [in]

The handle of a device context that was previously obtained by <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a>.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



<b>ReleaseDC</b> also unlocks the surface that was previously locked when the <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a> method was called.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>ReleaseDC</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

