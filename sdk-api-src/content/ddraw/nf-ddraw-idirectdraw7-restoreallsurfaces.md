---
UID: NF:ddraw.IDirectDraw7.RestoreAllSurfaces
title: IDirectDraw7::RestoreAllSurfaces
author: windows-sdk-content
description: Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.
old-location: directdraw\idirectdraw7_restoreallsurfaces.htm
old-project: directdraw
ms.assetid: 72897004-cd44-4ca4-bc28-a49bffc09c76
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],RestoreAllSurfaces method, IDirectDraw7.RestoreAllSurfaces, IDirectDraw7::RestoreAllSurfaces, RestoreAllSurfaces, RestoreAllSurfaces method [DirectDraw], RestoreAllSurfaces method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::RestoreAllSurfaces, directdraw.idirectdraw7_restoreallsurfaces
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDraw7.RestoreAllSurfaces
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::RestoreAllSurfaces


## -description


 Restores all the surfaces that were created for the DirectDraw object, in the order that they were created.



## -parameters






## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



This method is provided for convenience. Effectively, this method calls the <a href="https://msdn.microsoft.com/9ca7abb2-5b9a-4323-9f0b-952e183e794b">IDirectDrawSurface7::Restore</a> method for each surface that is created by this DirectDraw object.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>RestoreAllSurfaces</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

