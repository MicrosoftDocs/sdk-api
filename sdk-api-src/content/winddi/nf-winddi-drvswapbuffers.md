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

# DrvSwapBuffers function


## -description


The <b>DrvSwapBuffers</b> function displays the contents of the window's associated hidden buffer on the specified surface.


## -parameters




### -param pso

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that identifies the target surface to be modified for display.


### -param pwo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure that defines the region on the target surface with which the back buffer will be swapped.


## -returns



The return value is <b>TRUE</b> if the function is successful; it is <b>FALSE</b> upon failure.




## -remarks



<b>DrvSwapBuffers</b> can affect the display only if the pixel format for the window specified by <i>pwo</i> is double-buffered. The content of the hidden buffer is undefined after the swap occurs.

This function is required if the driver supports a pixel format with double buffering; that is, if PFD_DOUBLEBUFFER is set in the <b>dwFlags</b> member of the PIXELFORMATDESCRIPTOR structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556190">DrvDescribePixelFormat</a>
 

 

