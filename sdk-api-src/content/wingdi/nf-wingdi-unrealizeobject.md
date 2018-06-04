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

# UnrealizeObject function


## -description


The <b>UnrealizeObject</b> function resets the origin of a brush or resets a logical palette. If the <i>hgdiobj</i> parameter is a handle to a brush, <b>UnrealizeObject</b> directs the system to reset the origin of the brush the next time it is selected. If the <i>hgdiobj</i> parameter is a handle to a logical palette, <b>UnrealizeObject</b> directs the system to realize the palette as though it had not previously been realized. The next time the application calls the <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function for the specified palette, the system completely remaps the logical palette to the system palette.


## -parameters




### -param h

TBD




#### - hgdiobj [in]

A handle to the logical palette to be reset.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>UnrealizeObject</b> function should not be used with stock objects. For example, the default palette, obtained by calling <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> (DEFAULT_PALETTE), is a stock object.

A palette identified by <i>hgdiobj</i> can be the currently selected palette of a device context.


         If <i>hgdiobj</i> is a brush, <b>UnrealizeObject</b> does nothing, and the function returns <b>TRUE</b>. Use <a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a> to set the origin of a brush.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>
 

 

