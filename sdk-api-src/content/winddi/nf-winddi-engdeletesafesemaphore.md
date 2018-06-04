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

# EngDeleteSafeSemaphore function


## -description


The <b>EngDeleteSafeSemaphore</b> function removes a reference to the specified safe semaphore.


## -parameters




### -param pssem [in, out]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a> structure that contains the safe semaphore from which to delete a reference.


## -returns



None




## -remarks



<b>EngDeleteSafeSemaphore</b> deletes the semaphore only when the last reference to it has been removed.


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564959">EngInitializeSafeSemaphore</a> and <b>EngDeleteSafeSemaphore</b> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Every caller of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when it no longer needs the semaphore.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564959">EngInitializeSafeSemaphore</a>
 

 

