---
UID: NF:winddi.EngIsSemaphoreOwnedByCurrentThread
title: EngIsSemaphoreOwnedByCurrentThread function
author: windows-sdk-content
description: The EngIsSemaphoreOwnedByCurrentThread function determines whether the currently executing thread holds the specified semaphore.
old-location: display\engissemaphoreownedbycurrentthread.htm
tech.root: display
ms.assetid: ce5d8ceb-0137-4ca9-b718-2e3de650249d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EngIsSemaphoreOwnedByCurrentThread, EngIsSemaphoreOwnedByCurrentThread function [Display Devices], display.engissemaphoreownedbycurrentthread, gdifncs_6c3dcc33-1798-4dc5-a64f-a9bb85f5cf81.xml, winddi/EngIsSemaphoreOwnedByCurrentThread
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
 - EngIsSemaphoreOwnedByCurrentThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EngIsSemaphoreOwnedByCurrentThread
: 
---

# EngIsSemaphoreOwnedByCurrentThread function


## -description


The <b>EngIsSemaphoreOwnedByCurrentThread</b> function determines whether the currently executing thread holds the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore.


## -returns



<b>EngIsSemaphoreOwnedByCurrentThread</b> returns <b>TRUE</b> if the currently executing thread holds the specified semaphore, and <b>FALSE</b> if it does not.




## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/02b68914-5007-4bfb-ac8a-0269447ab26b">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/a04f6f46-f075-40d1-8b56-d37a80fb3571">EngIsSemaphoreOwned</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

