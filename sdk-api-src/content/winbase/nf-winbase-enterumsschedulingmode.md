---
UID: NF:winbase.EnterUmsSchedulingMode
title: EnterUmsSchedulingMode function
author: windows-sdk-content
description: Converts the calling thread into a user-mode scheduling (UMS) scheduler thread.
old-location: base\enterumsschedulingmode.htm
old-project: ProcThread
ms.assetid: 792bd7fa-0ae9-4c38-a664-5fb3e3d0c52b
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: EnterUmsSchedulingMode, EnterUmsSchedulingMode function, base.enterumsschedulingmode, winbase/EnterUmsSchedulingMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-ums-l1-1-0.dll
api_name:
-	EnterUmsSchedulingMode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnterUmsSchedulingMode function


## -description


Converts the calling thread into a user-mode scheduling (UMS) scheduler thread.


## -parameters




### -param SchedulerStartupInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/e3f7b1b7-d2b8-432d-bce7-3633292e855b">UMS_SCHEDULER_STARTUP_INFO</a> structure that specifies UMS attributes for the thread, including a completion list and a <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a>     entry point function.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



An application's UMS scheduler creates one UMS scheduler thread for each processor that will be used to run UMS threads. The scheduler typically sets the affinity of the scheduler thread for a single processor, effectively reserving the processor for the use of that scheduler thread. For more information about thread affinity, see <a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>.

When a UMS scheduler thread is created, the system calls the <a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a> entry point function specified with the <b>EnterUmsSchedulingMode</b> function call.  The application's scheduler is responsible for finishing any application-specific initialization of the scheduler thread and selecting a UMS worker thread to run.

The application's scheduler selects a UMS worker thread to run by calling <a href="https://msdn.microsoft.com/e4265351-e8e9-4878-bd42-93258b4cd1a0">ExecuteUmsThread</a> with the worker thread's UMS thread context. The worker thread runs until it yields control by calling <a href="https://msdn.microsoft.com/d7c94ed5-9536-4c39-8658-27e4237cc9ba">UmsThreadYield</a>, blocks, or terminates. The scheduler thread is then available to run another worker thread.

A scheduler thread should continue to run until all of its worker threads reach a natural stopping point: that is, all worker threads have yielded, blocked, or  terminated. 




## -see-also




<a href="https://msdn.microsoft.com/e4265351-e8e9-4878-bd42-93258b4cd1a0">ExecuteUmsThread</a>



<a href="https://msdn.microsoft.com/3c9186c8-a54d-4536-8237-bfff78cc7d11">Multiple Processors</a>



<a href="https://msdn.microsoft.com/e3f7b1b7-d2b8-432d-bce7-3633292e855b">UMS_SCHEDULER_STARTUP_INFO</a>



<a href="https://msdn.microsoft.com/10de1c48-255d-45c3-acf0-25f8a564b585">UmsSchedulerProc</a>



<a href="https://msdn.microsoft.com/f9dd92fe-6d7a-452c-893e-e6df1757e377">User-Mode Scheduling</a>
 

 

