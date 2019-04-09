---
UID: NF:fibersapi.IsThreadAFiber
title: IsThreadAFiber function
author: windows-sdk-content
description: Determines whether the current thread is a fiber.
old-location: base\isthreadafiber.htm
tech.root: ProcThread
ms.assetid: 0d591343-84eb-410d-815b-b42850d3f2e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsThreadAFiber, IsThreadAFiber function, base.isthreadafiber, fibersapi/IsThreadAFiber, winbase/IsThreadAFiber
ms.topic: function
req.header: fibersapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-fibers-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - IsThreadAFiber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsThreadAFiber function


## -description


Determines whether the current thread is a fiber.


## -parameters






## -returns



The function returns <b>TRUE</b> if the thread is a fiber and <b>FALSE</b> otherwise.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/cb0473f8-bc49-44c9-a8b7-6d5b55aa37a5">ConvertThreadToFiberEx</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

