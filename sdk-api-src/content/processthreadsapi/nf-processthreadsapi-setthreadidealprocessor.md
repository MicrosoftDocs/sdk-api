---
UID: NF:processthreadsapi.SetThreadIdealProcessor
title: SetThreadIdealProcessor function (processthreadsapi.h)
description: Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.helpviewer_keywords: ["SetThreadIdealProcessor","SetThreadIdealProcessor function","_win32_setthreadidealprocessor","base.setthreadidealprocessor","processthreadsapi/SetThreadIdealProcessor"]
old-location: base\setthreadidealprocessor.htm
tech.root: ProcThread
ms.assetid: b174f74b-4b61-4170-a8a6-2ddc4cc5e375
ms.date: 12/05/2018
ms.keywords: SetThreadIdealProcessor, SetThreadIdealProcessor function, _win32_setthreadidealprocessor, base.setthreadidealprocessor, processthreadsapi/SetThreadIdealProcessor
f1_keywords:
- processthreadsapi/SetThreadIdealProcessor
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadIdealProcessor function


## -description


Sets a preferred processor for a thread. The system schedules threads on their preferred processors whenever possible.

On a system with more than 64 processors, this function sets the preferred processor to a logical processor in the <a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">processor group</a> to which the calling thread is assigned. Use the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex">SetThreadIdealProcessorEx</a> function to specify a processor group and preferred processor.


## -parameters




### -param hThread [in]

A handle to the thread whose preferred processor is to be set. The handle must have the THREAD_SET_INFORMATION access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


### -param dwIdealProcessor [in]

The number of the preferred processor for the thread. This value is zero-based. If this parameter is MAXIMUM_PROCESSORS, the function returns the current ideal processor without changing it.


## -returns



If the function succeeds, the return value is the previous preferred processor.

If the function fails, the return value is (DWORD) – 1. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



You can use the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function to determine the number of processors on the computer. You can also use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a> function to check the processors on which the thread is allowed to run. Note that 
<b>GetProcessAffinityMask</b> returns a bitmask whereas 
<b>SetThreadIdealProcessor</b> uses an integer value to represent the processor.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthread">OpenThread</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask">SetThreadAffinityMask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex">SetThreadIdealProcessorEx</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-threads">Threads</a>
 

 

