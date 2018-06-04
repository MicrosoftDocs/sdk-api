---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DirectDrawCreateClipper function


## -description


Creates an instance of a DirectDrawClipper object that is not associated with a DirectDraw object.


## -parameters




### -param dwFlags [in]

Currently not used and must be set to 0.


### -param lplpDDClipper [out]

Address of a pointer to be filled with the address of the new DirectDrawClipper object.


### -param pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Currently, this function returns an error if this parameter is not NULL.


## -returns



If the function succeeds, the return value is DD_OK.



If it fails, the function can return one of the following error values:

<ul>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



You can call <b>DirectDrawCreateClipper</b> before any DirectDraw objects are created. Because these DirectDrawClipper objects are not owned by any DirectDraw object, they are not automatically released when an application's objects are released. If the application does not explicitly release the DirectDrawClipper objects, DirectDraw releases them when the application terminates.

To create a DirectDrawClipper object that is owned by a specific DirectDraw object, use the <a href="https://msdn.microsoft.com/123a07c0-d371-4d10-bff8-b5640bd3b920">IDirectDraw7::CreateClipper</a> method.



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>DirectDrawCreateClipper</b> function.



