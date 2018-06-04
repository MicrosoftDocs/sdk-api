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

# EngLockSurface function


## -description


The <b>EngLockSurface</b> function creates a user object for a given surface. This function gives drivers access to surfaces they create.


## -parameters




### -param hsurf

Handle to the surface to be locked.


## -returns



<b>EngLockSurface</b> returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure if the function is successful. Otherwise, this function returns <b>NULL</b>.




## -remarks



This function gives drivers access to surfaces they create.

The driver is responsible for unlocking the surface when it no longer needs it. Surfaces should be locked only for very short periods of time.

Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565422">EngUnlockSurface</a> function to unlock the surface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565422">EngUnlockSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

