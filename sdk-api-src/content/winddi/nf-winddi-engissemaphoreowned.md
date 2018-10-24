---
UID: NF:winddi.EngIsSemaphoreOwned
title: EngIsSemaphoreOwned function
author: windows-sdk-content
description: The EngIsSemaphoreOwned function determines whether any thread holds the specified semaphore.
old-location: display\engissemaphoreowned.htm
tech.root: display
ms.assetid: a04f6f46-f075-40d1-8b56-d37a80fb3571
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EngIsSemaphoreOwned, EngIsSemaphoreOwned function [Display Devices], display.engissemaphoreowned, gdifncs_9bf4c866-a563-4bc5-99d6-0189f10f0742.xml, winddi/EngIsSemaphoreOwned
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
 - EngIsSemaphoreOwned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngIsSemaphoreOwned function


## -description


The <b>EngIsSemaphoreOwned</b> function determines whether any thread holds the specified semaphore.


## -parameters




### -param hsem [in]

Handle to the semaphore.


## -returns



<b>EngIsSemaphoreOwned</b> returns <b>TRUE</b> if any thread holds the specified semaphore, and <b>FALSE</b> if no thread holds it.




## -see-also




<a href="https://msdn.microsoft.com/da13ff30-7817-4ed4-9791-2d205a260259">EngAcquireSemaphore</a>



<a href="https://msdn.microsoft.com/02b68914-5007-4bfb-ac8a-0269447ab26b">EngCreateSemaphore</a>



<a href="https://msdn.microsoft.com/ce5d8ceb-0137-4ca9-b718-2e3de650249d">EngIsSemaphoreOwnedByCurrentThread</a>



<a href="https://msdn.microsoft.com/e89a556f-4071-425b-b138-bfb7b49a5e8c">EngReleaseSemaphore</a>
 

 

