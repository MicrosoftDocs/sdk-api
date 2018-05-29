---
UID: NF:wingdi.GetWindowExtEx
title: GetWindowExtEx function
author: windows-sdk-content
description: This function retrieves the x-extent and y-extent of the window for the specified device context.
old-location: gdi\getwindowextex.htm
old-project: gdi
ms.assetid: 17f41fcb-c9a4-4b7e-acde-73450044413e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetWindowExtEx, GetWindowExtEx function [Windows GDI], _win32_GetWindowExtEx, gdi.getwindowextex, wingdi/GetWindowExtEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-L1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	GetWindowExtEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetWindowExtEx function


## -description


This function retrieves the x-extent and y-extent of the window for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpsize

TBD




#### - lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that receives the x- and y-extents in page-space units, that is, logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/e3fc188a-3796-497d-9d86-f116e9e48e30">GetViewportExtEx</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>
 

 

