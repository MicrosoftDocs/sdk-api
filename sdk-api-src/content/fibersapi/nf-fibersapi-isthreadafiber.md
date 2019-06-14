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
ms.custom: 19H1
---

# IsThreadAFiber function


## -description


Determines whether the current thread is a fiber.


## -parameters






## -returns



The function returns <b>TRUE</b> if the thread is a fiber and <b>FALSE</b> otherwise.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-convertthreadtofiberex">ConvertThreadToFiberEx</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

