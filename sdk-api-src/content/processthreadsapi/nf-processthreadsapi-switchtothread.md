---
UID: NF:processthreadsapi.SwitchToThread
title: SwitchToThread function
author: windows-driver-content
description: Causes the calling thread to yield execution to another thread that is ready to run on the current processor. The operating system selects the next thread to be executed.
old-location: base\switchtothread.htm
old-project: ProcThread
ms.assetid: d1e6d734-0c5b-4aa0-b1b3-220f2615e56b
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SwitchToThread, SwitchToThread function, _win32_switchtothread, base.switchtothread, processthreadsapi/SwitchToThread, winbase/SwitchToThread
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-1.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l1-1-0.dll
-	API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
-	SwitchToThread
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>



<a href="https://msdn.microsoft.com/b76d7af7-e3ec-4663-a9e7-832c01733c8c">Suspending Thread Execution</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

