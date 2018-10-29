---
UID: NF:ddraw.IDirectDrawSurface7.AddOverlayDirtyRect
title: IDirectDrawSurface7::AddOverlayDirtyRect
author: windows-sdk-content
description: The IDirectDrawSurface7::AddOverlayDirtyRect method is not currently implemented.
old-location: directdraw\idirectdrawsurface7_addoverlaydirtyrect.htm
tech.root: directdraw
ms.assetid: 4ddd02ff-9e7f-4962-8954-0032f23959cd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddOverlayDirtyRect, AddOverlayDirtyRect method [DirectDraw], AddOverlayDirtyRect method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],AddOverlayDirtyRect method, IDirectDrawSurface7.AddOverlayDirtyRect, IDirectDrawSurface7::AddOverlayDirtyRect, ddraw/IDirectDrawSurface7::AddOverlayDirtyRect, directdraw.idirectdrawsurface7_addoverlaydirtyrect
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
 - IDirectDrawSurface7.AddOverlayDirtyRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::AddOverlayDirtyRect


## -description


The <b>IDirectDrawSurface7::AddOverlayDirtyRect</b> method is not currently implemented.


## -parameters






#### - lpRect [in]

A pointer to a <b>RECT</b> structure for the rectangle to update.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDSURFACETYPE</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>AddOverlayDirtyRect</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

