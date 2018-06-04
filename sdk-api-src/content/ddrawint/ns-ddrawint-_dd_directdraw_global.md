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

# _DD_DIRECTDRAW_GLOBAL structure


## -description


The DD_DIRECTDRAW_GLOBAL structure contains driver information that describes the driver's device. 


## -struct-fields




### -field dhpdev

Handle to the driver's private <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


### -field dwReserved1

Reserved for use by the display driver.


### -field dwReserved2

Reserved for use by the display driver.


### -field lpDDVideoPortCaps

Points to an array of one or more <a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a> structures in which the driver should describe the DirectDraw <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> objects that it supports. The structures are allocated by DirectDraw; the number of structures is based on the value returned in the <b>dwMaxVideoPort</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>.

This member is <b>NULL</b> when the driver does not implement the VPE.


## -remarks



DirectDraw allocates memory for this structure. Only one DD_DIRECTDRAW_GLOBAL definition exists per device. In a multimonitor system, each device has its own unique DD_DIRECTDRAW_GLOBAL structure. 

The <b>dwReserved1</b> and <b>dwReserved2</b> members can be used as required by the driver. For example, a driver might store pointers to internal data structures in these members.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a>
 

 

