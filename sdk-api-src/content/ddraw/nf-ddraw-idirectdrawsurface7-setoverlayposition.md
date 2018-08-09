---
UID: NF:ddraw.IDirectDrawSurface7.SetOverlayPosition
title: IDirectDrawSurface7::SetOverlayPosition
author: windows-sdk-content
description: Changes the display coordinates of an overlay surface.
old-location: directdraw\idirectdrawsurface7_setoverlayposition.htm
old-project: directdraw
ms.assetid: 94bd79f8-ded2-4cfa-98c1-a03202d3e678
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],SetOverlayPosition method, IDirectDrawSurface7.SetOverlayPosition, IDirectDrawSurface7::SetOverlayPosition, SetOverlayPosition, SetOverlayPosition method [DirectDraw], SetOverlayPosition method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetOverlayPosition, directdraw.idirectdrawsurface7_setoverlayposition
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
 - IDirectDrawSurface7.SetOverlayPosition
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawSurface7::SetOverlayPosition


## -description


Changes the display coordinates of an overlay surface.



## -parameters




### -param






#### - lX [in]

The new x- display coordinate of this surface.


#### - lY [in]

The new y-display coordinate of this surface.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDPOSITION</li>
<li>DDERR_NOOVERLAYDEST</li>
<li>DDERR_NOTAOVERLAYSURFACE</li>
<li>DDERR_OVERLAYNOTVISIBLE</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetOverlayPosition</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

