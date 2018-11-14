---
UID: NF:winbase.GetProcessAffinityMask
title: GetProcessAffinityMask function
author: windows-sdk-content
description: Retrieves the process affinity mask for the specified process and the system affinity mask for the system.
old-location: base\getprocessaffinitymask.htm
tech.root: procthread
ms.assetid: f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetProcessAffinityMask, GetProcessAffinityMask function, _win32_getprocessaffinitymask, base.getprocessaffinitymask, winbase/GetProcessAffinityMask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetProcessAffinityMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetProcessAffinityMask
: 
---

# GetProcessAffinityMask function


## -description


Retrieves the process affinity mask for the specified process and the system affinity mask for the system.


## -parameters




### -param hProcess [in]

A handle to the process whose affinity mask is desired.

This handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.


### -param lpProcessAffinityMask [out]

A pointer to a variable that receives the affinity mask for the specified process.


### -param lpSystemAffinityMask [out]

A pointer to a variable that receives the affinity mask for the system.


## -returns



If the function succeeds, the return value is nonzero and the function sets the variables pointed to by <i>lpProcessAffinityMask</i> and <i>lpSystemAffinityMask</i> to the appropriate affinity masks.

On a system with more than 64 processors, if the threads of the calling process are in a single <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a>, the function sets the variables pointed to by <i>lpProcessAffinityMask</i> and <i>lpSystemAffinityMask</i> to the process affinity mask and the processor mask of active logical processors for that group. If the calling process contains threads in multiple groups, the function returns zero for both affinity masks.

If the function fails, the return value is zero, and the values of the variables pointed to by <i>lpProcessAffinityMask</i> and <i>lpSystemAffinityMask</i> are undefined. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A process affinity mask is a bit vector in which each bit represents the processors that a process is allowed to run on. A system affinity mask is a bit vector in which each bit represents the processors that are configured into a system.

A process affinity mask is a subset of the system affinity mask. A process is only allowed to run on the processors configured into a system. Therefore, the process affinity mask cannot specify a 1 bit for a processor when the system affinity mask specifies a 0 bit for that processor.




## -see-also




<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>



<a href="https://msdn.microsoft.com/210b4c95-4072-4039-aa4f-6b0d85758359">SetProcessAffinityMask</a>



<a href="https://msdn.microsoft.com/3390930d-026f-4f86-97bc-1da34bb384ba">SetThreadAffinityMask</a>
 

 

