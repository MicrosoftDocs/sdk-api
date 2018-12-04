---
UID: NF:winddi.EngCreateSemaphore
title: EngCreateSemaphore function
author: windows-sdk-content
description: The EngCreateSemaphore function creates a semaphore object.
old-location: display\engcreatesemaphore.htm
tech.root: display
ms.assetid: 02b68914-5007-4bfb-ac8a-0269447ab26b
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: EngCreateSemaphore, EngCreateSemaphore function [Display Devices], display.engcreatesemaphore, gdifncs_d0ae1b52-59e6-49a9-ab03-7ff1008dc5c6.xml, winddi/EngCreateSemaphore
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngCreateSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngCreateSemaphore function


## -description


The <b>EngCreateSemaphore</b> function creates a semaphore object.


## -parameters






## -returns



If the function succeeds, the return value is a handle to the semaphore object. A null pointer is returned if the function fails.




## -remarks



Graphics drivers can create and use a semaphore object for resource synchronization. For example:

<ul>
<li>
The <i>Permedia</i> display driver uses a semaphore when an asynchronous pointer requires access to the CRTC registers, because these registers are shared by both the asynchronous hardware pointers and the synchronous activities of the device.

</li>
<li>
Multiple printer drivers sharing global data, such as font data on a print server, need to synchronize access to this data.

</li>
</ul>
<div class="alert"><b>Note</b>  The Microsoft Windows Driver Kit (WDK) does not contain the 3Dlabs Permedia2 (<i>3dlabs.htm</i> ) and 3Dlabs Permedia3 (<i>Perm3.htm</i>) sample display drivers. You can get these sample drivers from the Windows Server 2003 SP1 Driver Development Kit (DDK), which you can download from the <a href="http://go.microsoft.com/fwlink/p/?linkid=21859">DDK - Windows Driver Development Kit</a> page of the WDHC website.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/6855017c-8919-496b-b82c-d65dea7ad5f0">EngDeleteSemaphore</a>



<a href="https://msdn.microsoft.com/a04f6f46-f075-40d1-8b56-d37a80fb3571">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/ce5d8ceb-0137-4ca9-b718-2e3de650249d">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

