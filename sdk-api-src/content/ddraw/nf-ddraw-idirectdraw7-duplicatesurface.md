---
UID: NF:ddraw.IDirectDraw7.DuplicateSurface
title: IDirectDraw7::DuplicateSurface
author: windows-sdk-content
description: Duplicates a DirectDrawSurface object.
old-location: directdraw\idirectdraw7_duplicatesurface.htm
old-project: directdraw
ms.assetid: 515219e9-95e9-41fd-9797-d143cd542ef6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DuplicateSurface, DuplicateSurface method [DirectDraw], DuplicateSurface method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],DuplicateSurface method, IDirectDraw7.DuplicateSurface, IDirectDraw7::DuplicateSurface, ddraw/IDirectDraw7::DuplicateSurface, directdraw.idirectdraw7_duplicatesurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.redist: 
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
 - IDirectDraw7.DuplicateSurface
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::DuplicateSurface


## -description


Duplicates a DirectDrawSurface object.



## -parameters




### -param






#### - lpDDSurface [in]

Address of the <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface for the surface to be duplicated.


#### - lplpDupDDSurface [out]

Address of a variable to contain an <a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a> interface pointer for the newly duplicated DirectDrawSurface object.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_CANTDUPLICATE</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_SURFACELOST</li>
</ul>



## -remarks



<b>DuplicateSurface</b> creates a new DirectDrawSurface object that points to the same surface memory as an existing DirectDrawSurface object. This duplicate can be used just like the original object. The surface memory is released after the last object referring to it is released. A primary surface, 3-D surface, or implicitly created surface cannot be duplicated.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>DuplicateSurface</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

