---
UID: NF:ddraw.IDirectDraw7.CreateClipper
title: IDirectDraw7::CreateClipper
author: windows-sdk-content
description: Creates a DirectDrawClipper object.
old-location: directdraw\idirectdraw7_createclipper.htm
old-project: directdraw
ms.assetid: 123a07c0-d371-4d10-bff8-b5640bd3b920
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: CreateClipper, CreateClipper method [DirectDraw], CreateClipper method [DirectDraw],IDirectDraw7 interface, IDirectDraw7 interface [DirectDraw],CreateClipper method, IDirectDraw7.CreateClipper, IDirectDraw7::CreateClipper, ddraw/IDirectDraw7::CreateClipper, directdraw.idirectdraw7_createclipper
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
 - IDirectDraw7.CreateClipper
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDraw7::CreateClipper


## -description


Creates a DirectDrawClipper object.


## -parameters




### -param






#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lplpDDClipper [out]

Address of a variable to be set to a valid <a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a> interface pointer if the call succeeds.


#### - pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Currently this method returns an error if this parameter is not NULL.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCOOPERATIVELEVELSET</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



The DirectDrawClipper object can be attached to a DirectDrawSurface and used during <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a>, <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a>, and <a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">IDirectDrawSurface7::UpdateOverlay</a> operations.

To create a DirectDrawClipper object that is not owned by a specific DirectDraw object, use the <a href="https://msdn.microsoft.com/12d499d2-dd4a-4831-9290-c225aec1a160">DirectDrawCreateClipper</a> function.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>CreateClipper</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

