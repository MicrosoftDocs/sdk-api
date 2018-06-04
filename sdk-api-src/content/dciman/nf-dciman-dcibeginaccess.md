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

# DCIBeginAccess function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Obtains an access pointer to display frame buffer based on the given rectangle.



## -parameters




### -param pdci [in]

A pointer to a <b>DCISURFACEINFO</b> structure.


### -param x [in]

The x-coordinate of the upper-left corner of the rectangle.


### -param y [in]

The y-coordinate of the upper-left corner of the rectangle.


### -param dx [in]

The width of the rectangle. 


### -param dy [in]

The height of the rectangle.


## -returns



If the function succeeds, the return value is DCI_OK or DCI_STATUS_POINTERCHANGED.  DCI_STATUS_POINTERCHANGED indicates that the virtual address of the frame buffer could have been changed since the last call.  So the application should not assume the consistency of the virtual address of the display frame buffer.  If the function fails, the return value is one of the DCI errors.
				
 




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

