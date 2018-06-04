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

# EngCreatePath function


## -description


The <b>EngCreatePath</b> function allocates a path for the driver's temporary use. 


## -parameters






## -returns



The return value is a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure if the function is successful. Otherwise, it is null, and an error code is logged.




## -remarks



The driver should delete the path, allocated by <b>EngCreatePath</b>, before returning to GDI from its current drawing call.

Functions that create and modify paths are provided to assist devices in clipping paths. A driver can create a path, fill it with lines and pass the path to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a> for clipping against the complex region.

A PATHOBJ structure is a locked object, and thus should not be locked for a long time by the driver.

If the driver uses <b>EngCreatePath</b> to create a PATHOBJ structure, it should be deleted by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564811">EngDeletePath</a> as soon as the driver finishes with it.

The returned PATHOBJ structure is used in calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568853">PATHOBJ_bMoveTo</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff568855">PATHOBJ_bPolyLineTo</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>
 

 

