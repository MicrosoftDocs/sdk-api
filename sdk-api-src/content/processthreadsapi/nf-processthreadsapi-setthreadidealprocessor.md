---
UID: NF:processthreadsapi.SetThreadIdealProcessor
title: SetThreadIdealProcessor function
author: windows-sdk-content
description: Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.
old-location: base\setthreadidealprocessor.htm
tech.root: ProcThread
ms.assetid: b174f74b-4b61-4170-a8a6-2ddc4cc5e375
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetThreadIdealProcessor, SetThreadIdealProcessor function, _win32_setthreadidealprocessor, base.setthreadidealprocessor, processthreadsapi/SetThreadIdealProcessor
ms.topic: function
req.header: processthreadsapi.h
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
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetThreadIdealProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadIdealProcessor function


## -description


Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.

On a system with more than 64 processors, this function sets the preferred processor to a logical processor in the <a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">processor group</a> to which the calling thread is assigned. Use the <a href="https://msdn.microsoft.com/6b599a99-41c5-45c7-8aeb-87d8f34e9e82">SetThreadIdealProcessorEx</a> function to specify a processor group and preferred processor.


## -parameters




### -param hThread [in]

A handle to the thread whose preferred processor is to be set. The handle must have the THREAD_SET_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param dwIdealProcessor [in]

The number of the preferred processor for the thread. This value is zero-based. If this parameter is MAXIMUM_PROCESSORS, the function returns the current ideal processor without changing it.


## -returns



If the function succeeds, the return value is the previous preferred processor.

If the function fails, the return value is (DWORD) – 1. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can use the <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function to determine the number of processors on the computer. You can also use the 
<a href="https://msdn.microsoft.com/f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f">GetProcessAffinityMask</a> function to check the processors on which the thread is allowed to run. Note that 
<b>GetProcessAffinityMask</b> returns a bitmask whereas 
<b>SetThreadIdealProcessor</b> uses an integer value to represent the processor.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/f50ca86e-fa81-4ed9-ae6c-63a4e7f2a53f">GetProcessAffinityMask</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/3390930d-026f-4f86-97bc-1da34bb384ba">SetThreadAffinityMask</a>



<a href="https://msdn.microsoft.com/6b599a99-41c5-45c7-8aeb-87d8f34e9e82">SetThreadIdealProcessorEx</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

