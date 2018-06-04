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

# PDD_SURFCB_DESTROYSURFACE callback function


## -description


The <b>DdDestroySurface</b> callback function destroys a DirectDraw surface.


## -parameters




### -param Arg1








#### - lpDestroySurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550577">DD_DESTROYSURFACEDATA</a> structure that contains the information needed to destroy a surface.


## -returns



<b>DdDestroySurface</b> returns one of the following callback codes:




## -remarks



If DirectDraw did the memory allocation at surface creation time and the driver was not involved in the allocation, DirectDraw does not call the driver's <b>DdDestroySurface</b> function to destroy the surface. 

If the driver is performing the surface memory management itself, <b>DdDestroySurface</b> should free the surface memory and perform any other cleanup, such as freeing private data stored in the <b>dwReserved1</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551726">DD_SURFACE_GLOBAL</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structures.

For a driver-managed surface, if the surface is persistent (that is, the DDSCAPS2_DONOTPERSIST flag in the <b>dwCaps2</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure for the surface is not set), <b>DdDestroySurface</b> can be called with the purpose of envicting the surface from video memory. In this case, the display driver can continue to keep any private data in the <b>dwReserved1</b> members until <b>DdDestroySurface</b> is called to actually destroy the surface.

<b>DdDestroySurface</b> can be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550577">DD_DESTROYSURFACEDATA</a>



<a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>
 

 

