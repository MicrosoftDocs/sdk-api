---
UID: NF:processthreadsapi.GetSystemTimes
title: GetSystemTimes function
author: windows-sdk-content
description: Retrieves system timing information. On a multiprocessor system, the values returned are the sum of the designated times across all processors.
old-location: base\getsystemtimes.htm
tech.root: sysinfo
ms.assetid: 84f674e7-536b-4ae0-b523-6a17cb0a1c17
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetSystemTimes, GetSystemTimes function, base.getsystemtimes, processthreadsapi/GetSystemTimes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetSystemTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemTimes function


## -description


Retrieves system timing information.  On a multiprocessor system, the values returned are the sum
    of the designated times across all processors.


## -parameters




### -param lpIdleTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the amount of time that the system has been idle.


### -param lpKernelTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors). This time value also includes the amount of time the system has been idle.


### -param lpUserTime [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors).


## -returns



If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error  information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>



<a href="https://msdn.microsoft.com/3733f611-c6a1-4d48-b21e-ada3490c5de1">Time Functions</a>
 

 

