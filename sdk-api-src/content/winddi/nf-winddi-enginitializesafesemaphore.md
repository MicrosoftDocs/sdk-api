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

# EngInitializeSafeSemaphore function


## -description


The <b>EngInitializeSafeSemaphore</b> function initializes the specified safe semaphore. 


## -parameters




### -param pssem [out]

Pointer to the driver-allocated <a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a> structure to be initialized.


## -returns



<b>EngInitializeSafeSemaphore</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



<b>EngInitializeSafeSemaphore</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff564814">EngDeleteSafeSemaphore</a> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Once the safe semaphore is initialized, the driver can call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a> with the <b>hsem</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a> structure for synchronization.

Callers of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when they no longer need the semaphore.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565007">ENGSAFESEMAPHORE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564174">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564814">EngDeleteSafeSemaphore</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564960">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564961">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565004">EngReleaseSemaphore</a>
 

 

