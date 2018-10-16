---
UID: NF:processthreadsapi.GetThreadPriorityBoost
title: GetThreadPriorityBoost function
author: windows-sdk-content
description: Retrieves the priority boost control state of the specified thread.
old-location: base\getthreadpriorityboost.htm
tech.root: procthread
ms.assetid: 44edf5e3-7543-482f-89ff-ae9daf495ff3
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetThreadPriorityBoost, GetThreadPriorityBoost function, _win32_getthreadpriorityboost, base.getthreadpriorityboost, processthreadsapi/GetThreadPriorityBoost, winbase/GetThreadPriorityBoost
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadPriorityBoost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadPriorityBoost function


## -description


Retrieves the priority boost control state of the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread. The handle must have the <b>THREAD_QUERY_INFORMATION</b> or <b>THREAD_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_QUERY_INFORMATION</b> access right.


### -param pDisablePriorityBoost [out]

A pointer to a variable that receives the priority boost control state. A value of TRUE indicates that dynamic boosting is disabled. A value of FALSE indicates normal behavior.


## -returns



If the function succeeds, the return value is nonzero. In that case, the variable pointed to by the <i>pDisablePriorityBoost</i> parameter receives the priority boost control state.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/bcc6cec7-2d85-4810-98d0-7d99486f4924">Priority Boosts</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>



<a href="https://msdn.microsoft.com/5cc16bfe-6792-40e8-91ef-6f54a38e6e33">SetThreadPriorityBoost</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

