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

# EngLockDriverObj function


## -description


The <b>EngLockDriverObj</b> function creates an exclusive lock on this object for the calling thread. 


## -parameters




### -param hdo

Handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a> structure to be locked by GDI.


## -returns



<b>EngLockDriverObj</b> returns a DRIVEROBJ structure if the function is successful. If the operation fails, it returns <b>NULL</b>. 




## -remarks



This function will fail if the handle is invalid, if the object is already locked by another thread, or if the handle is not owned by the calling process.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a>
 

 

