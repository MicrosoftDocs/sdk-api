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

# EngUnlockDirectDrawSurface function


## -description


The <b>EngUnlockDirectDrawSurface</b> function releases the lock on the specified surface.


## -parameters




### -param pSurface [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface to be unlocked.


## -returns



<b>EngUnlockDirectDrawSurface</b> returns <b>TRUE</b> when it successfully unlocks the specified surface. Otherwise, it returns <b>FALSE</b>.




## -remarks



The surface must previously have been locked by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564966">EngLockDirectDrawSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564966">EngLockDirectDrawSurface</a>
 

 

