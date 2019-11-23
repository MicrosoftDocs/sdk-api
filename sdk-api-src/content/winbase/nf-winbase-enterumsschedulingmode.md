---
UID: NF:winbase.EnterUmsSchedulingMode
title: EnterUmsSchedulingMode function (winbase.h)

description: Converts the calling thread into a user-mode scheduling (UMS) scheduler thread.
old-location: base\enterumsschedulingmode.htm
tech.root: ProcThread
ms.assetid: 792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b

ms.date: 12/05/2018
ms.keywords: EnterUmsSchedulingMode, EnterUmsSchedulingMode function, base.enterumsschedulingmode, winbase/EnterUmsSchedulingMode
ms.topic: function
f1_keywords:
- winbase/EnterUmsSchedulingMode
dev_langs:
 - c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- kernel32.dll
- API-MS-Win-Core-ums-l1-1-0.dll
api_name:
- EnterUmsSchedulingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnterUmsSchedulingMode function


## -description


Converts the calling thread into a user-mode scheduling (UMS) scheduler thread.


## -parameters




### -param SchedulerStartupInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-ums_scheduler_startup_info">UMS_SCHEDULER_STARTUP_INFO</a> structure that specifies UMS attributes for the thread, including a completion list and a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a>     entry point function.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



An application's UMS scheduler creates one UMS scheduler thread for each processor that will be used to run UMS threads. The scheduler typically sets the affinity of the scheduler thread for a single processor, effectively reserving the processor for the use of that scheduler thread. For more information about thread affinity, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>.

When a UMS scheduler thread is created, the system calls the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> entry point function specified with the <b>EnterUmsSchedulingMode</b> function call.  The application's scheduler is responsible for finishing any application-specific initialization of the scheduler thread and selecting a UMS worker thread to run.

The application's scheduler selects a UMS worker thread to run by calling <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-executeumsthread">ExecuteUmsThread</a> with the worker thread's UMS thread context. The worker thread runs until it yields control by calling <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-umsthreadyield">UmsThreadYield</a>, blocks, or terminates. The scheduler thread is then available to run another worker thread.

A scheduler thread should continue to run until all of its worker threads reach a natural stopping point: that is, all worker threads have yielded, blocked, or  terminated. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-executeumsthread">ExecuteUmsThread</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-ums_scheduler_startup_info">UMS_SCHEDULER_STARTUP_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/user-mode-scheduling">User-Mode Scheduling</a>
 

 

