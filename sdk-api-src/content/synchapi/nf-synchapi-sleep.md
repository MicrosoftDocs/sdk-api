---
UID: NF:synchapi.Sleep
title: Sleep function
author: windows-sdk-content
description: Suspends the execution of the current thread until the time-out interval elapses.
old-location: base\sleep.htm
old-project: procthread
ms.assetid: 934d37ea-402c-4118-bd7e-87b5fce80fca
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Sleep, Sleep function, _win32_sleep, base.sleep, synchapi/Sleep, winbase/Sleep
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
tech.root: 
req.typenames: ITEMPROP, *LPITEMPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - Sleep
product: Windows
targetos: Windows
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
req.product: Windows XP with SP1 and later
---

# Sleep function


## -description


Suspends the execution of the current thread until the time-out interval elapses.

To enter an alertable wait state, use the 
<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a> function.


## -parameters




### -param dwMilliseconds [in]

The time interval for which execution is to be suspended, in milliseconds.

A value of zero causes the thread to relinquish the remainder of its time slice to any other thread  that is ready to run. If there are no other threads ready to run, the function returns immediately, and the thread continues execution.<b>Windows XP:  </b>A value of zero causes the thread to relinquish the remainder of its time slice to any other thread of equal priority that is ready to run. If there are no other threads of equal priority ready to run, the function returns immediately, and the thread continues execution. This behavior changed starting with Windows Server 2003.



A value of INFINITE indicates that the suspension should not time out.


## -returns



This function does not return a value.




## -remarks



This function causes a thread to relinquish the remainder of its time slice and become unrunnable for an interval based on the value of <i>dwMilliseconds</i>. The system clock "ticks" at a constant rate. If <i>dwMilliseconds</i> is less than the resolution of the system clock, the thread may sleep for less than the specified length of time. If <i>dwMilliseconds</i> is greater than one tick but less than two, the wait can be anywhere between one and two ticks, and so on. To increase the accuracy of the sleep interval, call the <b>timeGetDevCaps</b> function to determine the supported minimum timer resolution and the <b>timeBeginPeriod</b> function to set the timer resolution to its minimum. Use caution when calling <b>timeBeginPeriod</b>, as frequent calls can significantly affect the system clock, system power usage, and the scheduler. If you call <b>timeBeginPeriod</b>, call it one time early in the application and be sure to call the <b>timeEndPeriod</b> function at the very end of the application.

After the sleep interval has passed, the thread is ready to run. If you specify 0 milliseconds, the thread will relinquish the remainder of its time slice but remain ready. Note that a ready thread is not guaranteed to run immediately. Consequently, the thread may not run until some time after the sleep interval elapses. For more information, see 
<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>.

Be careful when using <b>Sleep</b> in the following scenarios:

<ul>
<li>Code  that directly or indirectly creates windows (for example, DDE and COM <b>CoInitialize</b>). If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. If you have a thread that uses 
<b>Sleep</b> with infinite delay, the system will deadlock. </li>
<li>Threads that are under concurrency control. For example, an I/O completion port or thread pool limits the number of associated threads that can run. If the maximum number of threads is already running, no additional associated thread can run until a running thread finishes. If a thread uses <b>Sleep</b> with an interval of zero to wait for one of the additional associated threads to accomplish some work,  the process might deadlock. </li>
</ul>
 For these scenarios, use 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> or 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>Sleep</b>.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b7f5a206-a827-4b6b-86f6-5e3aea1246b7">Using Thread Local Storage</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a>



<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>



<a href="https://msdn.microsoft.com/b76d7af7-e3ec-4663-a9e7-832c01733c8c">Suspending Thread Execution</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>



<a href="https://msdn.microsoft.com/d40de436-f71e-47f6-a8c3-549c2699eb4c">WaitOnAddress</a>
 

 

