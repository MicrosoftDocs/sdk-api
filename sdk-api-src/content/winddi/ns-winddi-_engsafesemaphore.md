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

# _ENGSAFESEMAPHORE structure


## -description


The ENGSAFESEMAPHORE structure provides the driver with a thread-safe semaphore.


## -struct-fields




### -field hsem

Handle to the semaphore.


### -field lCount

Specifies the reference count on the semaphore.


## -remarks



A safe semaphore is a wrapper that contains a handle to a semaphore and a reference count on that semaphore.

The driver allocates an ENGSAFESEMAPHORE structure and passes it to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564959">EngInitializeSafeSemaphore</a> for initialization. GDI operates the safe semaphore under a lock and maintains a reference count on it, making it suitable for multithreading.

Once the safe semaphore is initialized, the driver can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a> with the <b>hsem</b> for synchronization.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564814">EngDeleteSafeSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564959">EngInitializeSafeSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

