---
UID: NF:winbase.SetThreadAffinityMask
title: SetThreadAffinityMask function
author: windows-sdk-content
description: Sets a processor affinity mask for the specified thread.
old-location: base\setthreadaffinitymask.htm
old-project: procthread
ms.assetid: 3390930d-026f-4f86-97bc-1da34bb384ba
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetThreadAffinityMask, SetThreadAffinityMask function, _win32_setthreadaffinitymask, base.setthreadaffinitymask, winbase/SetThreadAffinityMask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-l1-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetThreadAffinityMask
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetThreadAffinityMask function


## -description


Sets a processor affinity mask for the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread whose affinity mask is to be set.

This handle must have the <b>THREAD_SET_INFORMATION</b> or <b>THREAD_SET_LIMITED_INFORMATION</b> access right and the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_SET_INFORMATION</b> and <b>THREAD_QUERY_INFORMATION</b> access rights.


### -param dwThreadAffinityMask [in]

The affinity mask for the thread.

On a system with more than 64 processors, the affinity mask must specify processors in the thread's current <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a>. 


## -returns



If the function succeeds, the return value is the thread's previous affinity mask.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the thread affinity mask requests a processor that is not selected for the process affinity mask, the last error code is <b>ERROR_INVALID_PARAMETER</b>.




## -remarks



A thread affinity mask is a bit vector in which each bit represents a logical processor that a thread is allowed to run on. A thread affinity mask must be a subset of the process affinity mask for the containing process of a thread. A thread can only run on the processors its process can run on. Therefore, the thread affinity mask cannot specify a 1 bit for a processor when the process affinity mask specifies a 0 bit for that processor.

Setting an affinity mask for a process or thread can result in threads receiving less processor time, as the system is restricted from running the threads on certain processors. In most cases, it is better to let the system select an available processor.

If the new thread affinity mask does not specify the processor that is currently running the thread, the thread is rescheduled on one of the allowable processors.




## -see-also




<a href="https://msdn.microsoft.com/f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f">GetProcessAffinityMask</a>



<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>



<a href="https://msdn.microsoft.com/210b4c95-4072-4039-aa4f-6b0d85758359">SetProcessAffinityMask</a>



<a href="https://msdn.microsoft.com/b174f74b-4b61-4170-a8a6-2ddc4cc5e375">SetThreadIdealProcessor</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

