---
UID: NC:ddrawint.PDD_SURFCB_DESTROYSURFACE
title: PDD_SURFCB_DESTROYSURFACE
author: windows-sdk-content
description: The DdDestroySurface callback function destroys a DirectDraw surface.
old-location: display\dddestroysurface.htm
old-project: display
ms.assetid: 90060863-02ef-49bf-820d-b3adffbc8f40
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdDestroySurface, DdDestroySurface callback function [Display Devices], PDD_SURFCB_DESTROYSURFACE, PDD_SURFCB_DESTROYSURFACE callback, ddfncs_f6029f7a-5729-42d3-8ff6-f5e27994b133.xml, ddrawint/DdDestroySurface, display.dddestroysurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Desktop
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdDestroySurface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_SURFCB_DESTROYSURFACE callback function


## -description


The <b>DdDestroySurface</b> callback function destroys a DirectDraw surface.


## -parameters




### -param Arg1








#### - lpDestroySurface

Points to a <a href="https://msdn.microsoft.com/77d9544d-72df-4e7d-ba57-644aeee34a88">DD_DESTROYSURFACEDATA</a> structure that contains the information needed to destroy a surface.


## -returns



<b>DdDestroySurface</b> returns one of the following callback codes:




## -remarks



If DirectDraw did the memory allocation at surface creation time and the driver was not involved in the allocation, DirectDraw does not call the driver's <b>DdDestroySurface</b> function to destroy the surface. 

If the driver is performing the surface memory management itself, <b>DdDestroySurface</b> should free the surface memory and perform any other cleanup, such as freeing private data stored in the <b>dwReserved1</b> members of the <a href="https://msdn.microsoft.com/11e0a6b9-16b9-4fc3-8e17-776f56c12196">DD_SURFACE_GLOBAL</a> and <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structures.

For a driver-managed surface, if the surface is persistent (that is, the DDSCAPS2_DONOTPERSIST flag in the <b>dwCaps2</b> member of the <a href="https://msdn.microsoft.com/023b1a6d-3f08-43cc-b9c0-9d312b347a6b">DDSCAPS2</a> structure for the surface is not set), <b>DdDestroySurface</b> can be called with the purpose of envicting the surface from video memory. In this case, the display driver can continue to keep any private data in the <b>dwReserved1</b> members until <b>DdDestroySurface</b> is called to actually destroy the surface.

<b>DdDestroySurface</b> can be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/29846ffd-b721-4d61-9983-07a2575f9fe8">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/023b1a6d-3f08-43cc-b9c0-9d312b347a6b">DDSCAPS2</a>



<a href="https://msdn.microsoft.com/77d9544d-72df-4e7d-ba57-644aeee34a88">DD_DESTROYSURFACEDATA</a>



<a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>
 

 

