---
UID: NF:winddi.EngInitializeSafeSemaphore
title: EngInitializeSafeSemaphore function
author: windows-sdk-content
description: The EngInitializeSafeSemaphore function initializes the specified safe semaphore.
old-location: display\enginitializesafesemaphore.htm
tech.root: display
ms.assetid: 17b614b0-1c41-442c-b787-978eac3ade45
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EngInitializeSafeSemaphore, EngInitializeSafeSemaphore function [Display Devices], display.enginitializesafesemaphore, gdifncs_92f07217-a6d2-4996-99a9-eb289a713e19.xml, winddi/EngInitializeSafeSemaphore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngInitializeSafeSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngInitializeSafeSemaphore function


## -description


The <b>EngInitializeSafeSemaphore</b> function initializes the specified safe semaphore. 


## -parameters




### -param pssem [out]

Pointer to the driver-allocated <a href="https://msdn.microsoft.com/225ca482-6a45-4726-b51b-57fa76b8c5b0">ENGSAFESEMAPHORE</a> structure to be initialized.


## -returns



<b>EngInitializeSafeSemaphore</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



<b>EngInitializeSafeSemaphore</b> and <a href="https://msdn.microsoft.com/d4789803-2343-4d9a-a146-79206d88d59e">EngDeleteSafeSemaphore</a> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Once the safe semaphore is initialized, the driver can call <a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a> and <a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a> with the <b>hsem</b> member of the <a href="https://msdn.microsoft.com/225ca482-6a45-4726-b51b-57fa76b8c5b0">ENGSAFESEMAPHORE</a> structure for synchronization.

Callers of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when they no longer need the semaphore.




## -see-also




<a href="https://msdn.microsoft.com/225ca482-6a45-4726-b51b-57fa76b8c5b0">ENGSAFESEMAPHORE</a>



<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/d4789803-2343-4d9a-a146-79206d88d59e">EngDeleteSafeSemaphore</a>



<a href="https://msdn.microsoft.com/a04f6f46-f075-40d1-8b56-d37a80fb3571">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/ce5d8ceb-0137-4ca9-b718-2e3de650249d">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

