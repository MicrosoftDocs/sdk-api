---
UID: NF:ddraw.IDirectDrawSurface7.GetSurfaceDesc
title: IDirectDrawSurface7::GetSurfaceDesc
author: windows-sdk-content
description: Retrieves a description of this surface in its current condition.
old-location: directdraw\idirectdrawsurface7_getsurfacedesc.htm
tech.root: directdraw
ms.assetid: 4c36685e-8eb7-4d91-a479-8f099d5e712b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetSurfaceDesc, GetSurfaceDesc method [DirectDraw], GetSurfaceDesc method [DirectDraw],IDirectDrawSurface7 interface, IDirectDrawSurface7 interface [DirectDraw],GetSurfaceDesc method, IDirectDrawSurface7.GetSurfaceDesc, IDirectDrawSurface7::GetSurfaceDesc, ddraw/IDirectDrawSurface7::GetSurfaceDesc, directdraw.idirectdrawsurface7_getsurfacedesc
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
 - IDirectDrawSurface7.GetSurfaceDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::GetSurfaceDesc


## -description


Retrieves a description of this surface in its current condition.


## -parameters






#### - lpDDSurfaceDesc [in, out]

A pointer to a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that receives the current description of this surface. You need only initialize this structure's <b>dwSize</b> member to the size, in bytes, of the structure prior to the call; no other preparation is required.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetSurfaceDesc</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

