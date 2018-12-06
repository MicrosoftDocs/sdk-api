---
UID: NF:winddi.EngDeleteSemaphore
title: EngDeleteSemaphore function
author: windows-sdk-content
description: The EngDeleteSemaphore function deletes a semaphore object from the system's resource list.
old-location: display\engdeletesemaphore.htm
tech.root: display
ms.assetid: 6855017c-8919-496b-b82c-d65dea7ad5f0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngDeleteSemaphore, EngDeleteSemaphore function [Display Devices], display.engdeletesemaphore, gdifncs_a669ceb3-f9b3-4940-b1f8-17c55ee42f59.xml, winddi/EngDeleteSemaphore
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
 - EngDeleteSemaphore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngDeleteSemaphore function


## -description


The <b>EngDeleteSemaphore</b> function deletes a semaphore object from the system's resource list.


## -parameters




### -param hsem [in]

Handle to the semaphore to be deleted. The semaphore was created in <a href="https://msdn.microsoft.com/02b68914-5007-4bfb-ac8a-0269447ab26b">EngCreateSemaphore</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/02b68914-5007-4bfb-ac8a-0269447ab26b">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

