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

# _WNDOBJ structure


## -description


The WNDOBJ structure allows the driver to keep track of the position, size, and visible client region changes of a window. 


## -struct-fields




### -field coClient

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure that describes the client region of the window. If <b>iDComplexity</b> is DC_RECT and the left edge in <b>rclBounds</b> is greater than or equal to the right edge, or the top edge is greater than or equal to the bottom edge, the client region is invisible.


### -field pvConsumer

Pointer to a driver-defined value that identifies this particular WNDOBJ structure. This value can be set by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570606">WNDOBJ_vSetConsumer</a> function.


### -field rclClient

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that describes the client area of the window in screen coordinates. This rectangle is lower-right exclusive, which means that the lower and right-hand edges of this region are not included.


### -field psoOwner

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that was passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a> when this WNDOBJ was created.


## -remarks



The visible client region can be enumerated by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570603">WNDOBJ_cEnumStart</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a> functions.

A driver can associate its own data with a WNDOBJ by calling the <b>WNDOBJ_vSetConsumer</b> function.

As an accelerator, the driver can access public members of the WNDOBJ. These public members are guaranteed to remain unchanged only in the context of the driver callback routine supplied to GDI in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a> function, or the functions where a WNDOBJ is given.

The driver should use the SURFOBJ to which <b>psoOwner</b> points to retrieve driver-specific state relevant to the WNDOBJ, such as the driver's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> handle, rather than maintain global variables.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570601">WNDOBJCHANGEPROC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570603">WNDOBJ_cEnumStart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570606">WNDOBJ_vSetConsumer</a>
 

 

