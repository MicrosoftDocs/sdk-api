---
UID: NF:winddi.EngReleaseSemaphore
title: EngReleaseSemaphore function (winddi.h)
author: windows-sdk-content
description: The EngReleaseSemaphore function releases the specified semaphore.
old-location: display\engreleasesemaphore.htm
tech.root: display
ms.assetid: e89a556f-4071-425b-b138-bfb7b49a5e8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngReleaseSemaphore, EngReleaseSemaphore function [Display Devices], display.engreleasesemaphore, gdifncs_e4181ebe-43c7-4a59-8f19-e1c37f89524b.xml, winddi/EngReleaseSemaphore
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngReleaseSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngReleaseSemaphore function


## -description


The <b>EngReleaseSemaphore</b> function releases the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore to be released.


## -returns



None




## -remarks



<b>EngReleaseSemaphore</b> releases the semaphore's exclusive lock on a driver's resource and reenables the delivery of special kernel asynchronous procedure calls.

The lock and asynchronous procedure call suspension were acquired in a call to <a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>.




## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/6855017c-8919-496b-b82c-d65dea7ad5f0">EngDeleteSemaphore</a>



<a href="https://msdn.microsoft.com/a04f6f46-f075-40d1-8b56-d37a80fb3571">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/ce5d8ceb-0137-4ca9-b718-2e3de650249d">EngIsSemaphoreOwnedByCurrentThread</a>
 

 

