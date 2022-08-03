---
UID: NF:synchapi.Sleep
title: Sleep function (synchapi.h)
description: Suspends the execution of the current thread until the time-out interval elapses.
helpviewer_keywords: ["Sleep","Sleep function","_win32_sleep","base.sleep","synchapi/Sleep","winbase/Sleep"]
old-location: base\sleep.htm
tech.root: base
ms.assetid: 934d37ea-402c-4118-bd7e-87b5fce80fca
ms.date: 12/05/2018
ms.keywords: Sleep, Sleep function, _win32_sleep, base.sleep, synchapi/Sleep, winbase/Sleep
req.header: synchapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Sleep
 - synchapi/Sleep
dev_langs:
 - c++
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
---

# Sleep function


## -description

Suspends the execution of the current thread until the time-out interval elapses.

To enter an alertable wait state, use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a> function.

## -parameters

### -param dwMilliseconds [in]

The time interval for which execution is to be suspended, in milliseconds.

A value of zero causes the thread to relinquish the remainder of its time slice to any other thread  that is ready to run. If there are no other threads ready to run, the function returns immediately, and the thread continues execution. <b>Windows XP:</b> A value of zero causes the thread to relinquish the remainder of its time slice to any other thread of equal priority that is ready to run. If there are no other threads of equal priority ready to run, the function returns immediately, and the thread continues execution. This behavior changed starting with Windows Server 2003.



A value of INFINITE indicates that the suspension should not time out.

## -remarks

This function causes a thread to relinquish the remainder of its time slice and become unrunnable for an interval based on the value of <i>dwMilliseconds</i>. The system clock "ticks" at a constant rate. If <i>dwMilliseconds</i> is less than the resolution of the system clock, the thread may sleep for less than the specified length of time. If <i>dwMilliseconds</i> is greater than one tick but less than two, the wait can be anywhere between one and two ticks, and so on. To increase the accuracy of the sleep interval, call the <b>timeGetDevCaps</b> function to determine the supported minimum timer resolution and the <b>timeBeginPeriod</b> function to set the timer resolution to its minimum. Use caution when calling <b>timeBeginPeriod</b>, as frequent calls can significantly affect the system clock, system power usage, and the scheduler. If you call <b>timeBeginPeriod</b>, call it one time early in the application and be sure to call the <b>timeEndPeriod</b> function at the very end of the application.

After the sleep interval has passed, the thread is ready to run. If you specify 0 milliseconds, the thread will relinquish the remainder of its time slice but remain ready. Note that a ready thread is not guaranteed to run immediately. Consequently, the thread may not run until some time after the sleep interval elapses. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

Be careful when using <b>Sleep</b> in the following scenarios:

<ul>
<li>Code  that directly or indirectly creates windows (for example, DDE and COM <b>CoInitialize</b>). If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. If you have a thread that uses 
<b>Sleep</b> with infinite delay, the system will deadlock. </li>
<li>Threads that are under concurrency control. For example, an I/O completion port or thread pool limits the number of associated threads that can run. If the maximum number of threads is already running, no additional associated thread can run until a running thread finishes. If a thread uses <b>Sleep</b> with an interval of zero to wait for one of the additional associated threads to accomplish some work,  the process might deadlock. </li>
</ul>
 For these scenarios, use 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>Sleep</b>.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

For an example, see 
<a href="/windows/desktop/ProcThread/using-thread-local-storage">Using Thread Local Storage</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>



<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a>



<a href="/windows/desktop/ProcThread/suspending-thread-execution">Suspending Thread Execution</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitonaddress">WaitOnAddress</a>
