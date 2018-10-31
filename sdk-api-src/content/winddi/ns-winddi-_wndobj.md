---
UID: NS:winddi._WNDOBJ
title: "_WNDOBJ"
author: windows-sdk-content
description: The WNDOBJ structure allows the driver to keep track of the position, size, and visible client region changes of a window.
old-location: display\wndobj.htm
tech.root: display
ms.assetid: 69c47add-82a7-48fd-ae91-7756a6a8d15b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PWNDOBJ, PWNDOBJ, PWNDOBJ structure pointer [Display Devices], WNDOBJ, WNDOBJ structure [Display Devices], _WNDOBJ, display.wndobj, grstrcts_78a58771-627a-419e-b6f0-00411e32a22a.xml, winddi/PWNDOBJ, winddi/WNDOBJ"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - WNDOBJ
product: Windows
targetos: Windows
req.typenames: WNDOBJ, *PWNDOBJ
req.redist: 
---

# _WNDOBJ structure


## -description


The WNDOBJ structure allows the driver to keep track of the position, size, and visible client region changes of a window. 


## -struct-fields




### -field coClient

Specifies a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that describes the client region of the window. If <b>iDComplexity</b> is DC_RECT and the left edge in <b>rclBounds</b> is greater than or equal to the right edge, or the top edge is greater than or equal to the bottom edge, the client region is invisible.


### -field pvConsumer

Pointer to a driver-defined value that identifies this particular WNDOBJ structure. This value can be set by calling the <a href="https://msdn.microsoft.com/c7b550b8-1a3f-4d69-93d1-241044cb4bbd">WNDOBJ_vSetConsumer</a> function.


### -field rclClient

Specifies a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that describes the client area of the window in screen coordinates. This rectangle is lower-right exclusive, which means that the lower and right-hand edges of this region are not included.


### -field psoOwner

Pointer to the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that was passed to <a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a> when this WNDOBJ was created.


## -remarks



The visible client region can be enumerated by calling the <a href="https://msdn.microsoft.com/7d3951de-807f-4d54-a022-e2610987d965">WNDOBJ_cEnumStart</a> and <a href="https://msdn.microsoft.com/ad883ab5-6374-499e-9144-e5b85feaa471">WNDOBJ_bEnum</a> functions.

A driver can associate its own data with a WNDOBJ by calling the <b>WNDOBJ_vSetConsumer</b> function.

As an accelerator, the driver can access public members of the WNDOBJ. These public members are guaranteed to remain unchanged only in the context of the driver callback routine supplied to GDI in the <a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a> function, or the functions where a WNDOBJ is given.

The driver should use the SURFOBJ to which <b>psoOwner</b> points to retrieve driver-specific state relevant to the WNDOBJ, such as the driver's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> handle, rather than maintain global variables.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/14b1cced-32d0-4ba8-be7c-e626bef37e3f">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>



<a href="https://msdn.microsoft.com/09213eb9-df62-4da9-a221-3b50e66f5c68">WNDOBJCHANGEPROC</a>



<a href="https://msdn.microsoft.com/ad883ab5-6374-499e-9144-e5b85feaa471">WNDOBJ_bEnum</a>



<a href="https://msdn.microsoft.com/7d3951de-807f-4d54-a022-e2610987d965">WNDOBJ_cEnumStart</a>



<a href="https://msdn.microsoft.com/c7b550b8-1a3f-4d69-93d1-241044cb4bbd">WNDOBJ_vSetConsumer</a>
 

 

