---
UID: NF:wingdi.GetViewportExtEx
title: GetViewportExtEx function
author: windows-sdk-content
description: The GetViewportExtEx function retrieves the x-extent and y-extent of the current viewport for the specified device context.
old-location: gdi\getviewportextex.htm
tech.root: gdi
ms.assetid: e3fc188a-3796-497d-9d86-f116e9e48e30
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetViewportExtEx, GetViewportExtEx function [Windows GDI], _win32_GetViewportExtEx, gdi.getviewportextex, wingdi/GetViewportExtEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetViewportExtEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetViewportExtEx function


## -description


The <b>GetViewportExtEx</b> function retrieves the x-extent and y-extent of the current viewport for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpsize [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the x- and y-extents, in device units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/17f41fcb-c9a4-4b7e-acde-73450044413e">GetWindowExtEx</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>
 

 

