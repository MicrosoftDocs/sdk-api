---
UID: NF:ddraw.IDirectDraw7.GetGDISurface
title: IDirectDraw7::GetGDISurface
author: windows-sdk-content
description: Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.
old-location: directdraw\idirectdraw7_getgdisurface.htm
old-project: directdraw
ms.assetid: 4d0b827d-86f8-4d71-a193-9e330db0fbfd
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetGDISurface, GetGDISurface method [DirectDraw], GetGDISurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],GetGDISurface method, IDirectDraw7.GetGDISurface, IDirectDraw7::GetGDISurface, ddraw/IDirectDraw7::GetGDISurface, directdraw.idirectdraw7_getgdisurface
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDraw7.GetGDISurface
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::GetGDISurface


## -description


Retrieves the DirectDrawSurface object that currently represents the surface memory that GDI is treating as the primary surface.


## -parameters






#### - lplpGDIDDSSurface [out]

Address of a variable to be filled with a pointer to the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the surface that currently controls the GDI's primary surface memory.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOTFOUND</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>GetGDISurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

