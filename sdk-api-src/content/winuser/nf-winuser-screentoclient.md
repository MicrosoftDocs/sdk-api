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

# ScreenToClient function


## -description


The <b>ScreenToClient</b> function converts the screen coordinates of a specified point on the screen to client-area coordinates.


## -parameters




### -param hWnd [in]

A handle to the window whose client area will be used for the conversion.


### -param lpPoint

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that specifies the screen coordinates to be converted.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The function uses the window identified by the <i>hWnd</i> parameter and the screen coordinates given in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure to compute client coordinates. It then replaces the screen coordinates with the client coordinates. The new coordinates are relative to the upper-left corner of the specified window's client area.

The <b>ScreenToClient</b> function assumes the specified point is in screen coordinates.

All coordinates are in device units.

Do not use <b>ScreenToClient</b> when in a mirroring situation, that is, when changing from left-to-right layout to right-to-left layout. Instead, use <a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a>. For more information, see "Window Layout and Mirroring" in <a href="_win32_Window_Features_cpp">Window Features</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b1e2699-7f5f-444d-9072-f2ca7c8fa511">ClientToScreen</a>



<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/01c3b794-c1ca-467f-a4da-c6622453ee97">MapWindowPoints</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>
 

 

