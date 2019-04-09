---
UID: NS:winddi._ENGSAFESEMAPHORE
title: ENGSAFESEMAPHORE (winddi.h)
author: windows-sdk-content
description: The ENGSAFESEMAPHORE structure provides the driver with a thread-safe semaphore.
old-location: display\engsafesemaphore.htm
tech.root: display
ms.assetid: 225ca482-6a45-4726-b51b-57fa76b8c5b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ENGSAFESEMAPHORE, ENGSAFESEMAPHORE structure [Display Devices], display.engsafesemaphore, grstrcts_63b165c2-5032-4dcb-9039-562a38f24cc4.xml, winddi/ENGSAFESEMAPHORE
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - ENGSAFESEMAPHORE
product: Windows
targetos: Windows
req.typenames: ENGSAFESEMAPHORE
req.redist: 
---

# ENGSAFESEMAPHORE structure


## -description


The ENGSAFESEMAPHORE structure provides the driver with a thread-safe semaphore.


## -struct-fields




### -field hsem

Handle to the semaphore.


### -field lCount

Specifies the reference count on the semaphore.


## -remarks



A safe semaphore is a wrapper that contains a handle to a semaphore and a reference count on that semaphore.

The driver allocates an ENGSAFESEMAPHORE structure and passes it to <a href="https://msdn.microsoft.com/17b614b0-1c41-442c-b787-978eac3ade45">EngInitializeSafeSemaphore</a> for initialization. GDI operates the safe semaphore under a lock and maintains a reference count on it, making it suitable for multithreading.

Once the safe semaphore is initialized, the driver can call <a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a> and <a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a> with the <b>hsem</b> for synchronization.




## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/d4789803-2343-4d9a-a146-79206d88d59e">EngDeleteSafeSemaphore</a>



<a href="https://msdn.microsoft.com/17b614b0-1c41-442c-b787-978eac3ade45">EngInitializeSafeSemaphore</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

