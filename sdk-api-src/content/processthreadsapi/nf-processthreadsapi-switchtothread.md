---
UID: NF:processthreadsapi.SwitchToThread
title: SwitchToThread function (processthreadsapi.h)
description: Causes the calling thread to yield execution to another thread that is ready to run on the current processor. The operating system selects the next thread to be executed.
helpviewer_keywords: ["SwitchToThread","SwitchToThread function","_win32_switchtothread","base.switchtothread","processthreadsapi/SwitchToThread","winbase/SwitchToThread"]
old-location: base\switchtothread.htm
tech.root: backup
ms.assetid: d1e6d734-0c5b-4aa0-b1b3-220f2615e56b
ms.date: 12/05/2018
ms.keywords: SwitchToThread, SwitchToThread function, _win32_switchtothread, base.switchtothread, processthreadsapi/SwitchToThread, winbase/SwitchToThread
f1_keywords:
- processthreadsapi/SwitchToThread
dev_langs:
- c++
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
- SwitchToThread
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SwitchToThread function


## -description


Causes the calling thread to yield execution to another thread that is ready to run on the current processor. The operating system selects the next thread to be executed.


## -parameters






## -returns



If calling the 
<b>SwitchToThread</b> function causes the operating system to switch execution to another thread, the return value is nonzero.

If there are no other threads ready to execute, the operating system does not switch execution to another thread, and the return value is zero.




## -remarks



The yield of execution is in effect for up to one thread-scheduling time slice on the processor of the calling thread. The operating system will not switch execution to another processor, even if that processor is idle or is running a thread of lower priority. 

After the yielding thread's time slice elapses, the operating system reschedules execution for the yielding thread. The rescheduling is determined by the priority of the yielding thread and the status of other threads that are available to run.

Note that the operating system will not switch to a thread that is being prevented from running only by concurrency control. For example, an I/O completion port or thread pool limits the number of associated threads that can run. If the maximum number of threads is already running, no additional associated thread can run until a running thread finishes.   If a thread uses <b>SwitchToThread</b> to wait for one of the additional associated threads to accomplish some work, the process might deadlock.

To compile an application that uses this function, define _WIN32_WINNT as 0x0400 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread">SuspendThread</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/suspending-thread-execution">Suspending Thread Execution</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-threads">Threads</a>
 

 

