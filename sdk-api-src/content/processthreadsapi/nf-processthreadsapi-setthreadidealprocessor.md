---
UID: NF:processthreadsapi.SetThreadIdealProcessor
title: SetThreadIdealProcessor function (processthreadsapi.h)
description: Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.
helpviewer_keywords: ["SetThreadIdealProcessor","SetThreadIdealProcessor function","_win32_setthreadidealprocessor","base.setthreadidealprocessor","processthreadsapi/SetThreadIdealProcessor"]
old-location: base\setthreadidealprocessor.htm
tech.root: processthreadsapi
ms.assetid: b174f74b-4b61-4170-a8a6-2ddc4cc5e375
ms.date: 12/05/2018
ms.keywords: SetThreadIdealProcessor, SetThreadIdealProcessor function, _win32_setthreadidealprocessor, base.setthreadidealprocessor, processthreadsapi/SetThreadIdealProcessor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadIdealProcessor
 - processthreadsapi/SetThreadIdealProcessor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
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
---

# SetThreadIdealProcessor function


## -description

Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.

On a system with more than 64 processors, this function sets the preferred processor to a logical processor in the <a href="/windows/desktop/ProcThread/processor-groups">processor group</a> to which the calling thread is assigned. Use the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex">SetThreadIdealProcessorEx</a> function to specify a processor group and preferred processor.

## -parameters

### -param hThread [in]

A handle to the thread whose preferred processor is to be set. The handle must have the THREAD_SET_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param dwIdealProcessor [in]

The number of the preferred processor for the thread. This value is zero-based. If this parameter is MAXIMUM_PROCESSORS, the function returns the current ideal processor without changing it.

## -returns

If the function succeeds, the return value is the previous preferred processor.

If the function fails, the return value is (DWORD) – 1. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

You can use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function to determine the number of processors on the computer. You can also use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a> function to check the processors on which the thread is allowed to run. Note that 
<b>GetProcessAffinityMask</b> returns a bitmask whereas 
<b>SetThreadIdealProcessor</b> uses an integer value to represent the processor.

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default.
The <b>SetThreadIdealProcessor</b> function sets the preferred processor to a logical processor in the thread's primary group.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask">SetThreadAffinityMask</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex">SetThreadIdealProcessorEx</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>
