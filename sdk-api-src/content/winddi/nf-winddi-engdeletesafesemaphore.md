---
UID: NF:winddi.EngDeleteSafeSemaphore
title: EngDeleteSafeSemaphore function
author: windows-sdk-content
description: The EngDeleteSafeSemaphore function removes a reference to the specified safe semaphore.
old-location: display\engdeletesafesemaphore.htm
tech.root: display
ms.assetid: d4789803-2343-4d9a-a146-79206d88d59e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EngDeleteSafeSemaphore, EngDeleteSafeSemaphore function [Display Devices], display.engdeletesafesemaphore, gdifncs_ffbf0904-619e-48be-ada1-4269c8a92f55.xml, winddi/EngDeleteSafeSemaphore
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
 - EngDeleteSafeSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngDeleteSafeSemaphore function


## -description


The <b>EngDeleteSafeSemaphore</b> function removes a reference to the specified safe semaphore.


## -parameters




### -param pssem [in, out]

Pointer to the <a href="https://msdn.microsoft.com/225ca482-6a45-4726-b51b-57fa76b8c5b0">ENGSAFESEMAPHORE</a> structure that contains the safe semaphore from which to delete a reference.


## -returns



None




## -remarks



<b>EngDeleteSafeSemaphore</b> deletes the semaphore only when the last reference to it has been removed.


<a href="https://msdn.microsoft.com/17b614b0-1c41-442c-b787-978eac3ade45">EngInitializeSafeSemaphore</a> and <b>EngDeleteSafeSemaphore</b> are thread-safe, operating under a lock and maintaining a reference count on the semaphore. This guarantees that only one semaphore is created regardless of the number of simultaneous calls to it, and that the semaphore exists until the last reference to it is released.

Every caller of <b>EngInitializeSafeSemaphore</b> should call <b>EngDeleteSafeSemaphore</b> when it no longer needs the semaphore.




## -see-also




<a href="https://msdn.microsoft.com/225ca482-6a45-4726-b51b-57fa76b8c5b0">ENGSAFESEMAPHORE</a>



<a href="https://msdn.microsoft.com/17b614b0-1c41-442c-b787-978eac3ade45">EngInitializeSafeSemaphore</a>
 

 

