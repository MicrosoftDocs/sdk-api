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

# EngLockDirectDrawSurface function


## -description


The <b>EngLockDirectDrawSurface</b> function locks the kernel-mode handle of a DirectDraw surface.


## -parameters




### -param hSurface [in]

Handle to the surface to be locked.


## -returns



<b>EngLockDirectDrawSurface</b> returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface information upon success. Otherwise, it returns a <b>NULL</b> pointer.




## -remarks



<b>EngLockDirectDrawSurface</b> allows driver writers to lock DirectDraw surfaces. Locking the handle guarantees synchronized behavior and preserves the handle from being deleted by other threads in the system.

Currently, the driver receives DirectDraw surface handles only from the Direct3D texturing interface. Consequently, only drivers that perform texturing need to lock texture surfaces.

Upon completion of texturing, the driver must release the locked handle by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff565042">EngUnlockDirectDrawSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565042">EngUnlockDirectDrawSurface</a>
 

 

