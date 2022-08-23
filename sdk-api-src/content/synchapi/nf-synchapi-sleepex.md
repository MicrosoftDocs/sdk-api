---
UID: NF:synchapi.SleepEx
title: SleepEx function (synchapi.h)
description: Suspends the current thread until the specified condition is met.
helpviewer_keywords: ["SleepEx","SleepEx function","_win32_sleepex","base.sleepex","synchapi/SleepEx","winbase/SleepEx"]
old-location: base\sleepex.htm
tech.root: base
ms.assetid: a73cff94-ad63-4110-9f01-6469481c3d55
ms.date: 12/05/2018
ms.keywords: SleepEx, SleepEx function, _win32_sleepex, base.sleepex, synchapi/SleepEx, winbase/SleepEx
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
req.dll: KernelBase.dll on Windows Phone 8.1; Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SleepEx
 - synchapi/SleepEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KernelBase.dll
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SleepEx
---

# SleepEx function


## -description

Suspends the current thread until the specified condition is met. Execution resumes when one of the following occurs:
<ul>
<li>An I/O completion callback function is called.</li>
<li>An asynchronous procedure call (APC) is queued to the thread.</li>
<li>The time-out interval elapses.</li>
</ul>

## -parameters

### -param dwMilliseconds [in]

The time interval for which execution is to be suspended, in milliseconds.

A value of zero causes the thread to relinquish the remainder of its time slice to any other thread that is ready to run. If there are no other threads ready to run, the function returns immediately, and the thread continues execution.<b>Windows XP: </b>A value of zero causes the thread to relinquish the remainder of its time slice to any other thread of equal priority that is ready to run. If there are no other threads of equal priority ready to run, the function returns immediately, and the thread continues execution. This behavior changed starting with Windows Server 2003.



A value of INFINITE indicates that the suspension should not time out.

### -param bAlertable [in]

If this parameter is FALSE, the function does not return until the time-out period has elapsed. If an I/O completion callback occurs, the function does not immediately return and the I/O completion function is not executed. If an APC is queued to the thread, the function does not immediately return and the APC function is not executed.

If the parameter is TRUE and the thread that called this function is the same thread that called the extended I/O function (<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> or 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>), the function returns when either the time-out period has elapsed or when an I/O completion callback function occurs. If an I/O completion callback occurs, the I/O completion function is called. If an APC is queued to the thread (<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>), the function returns when either the time-out period has elapsed or when the APC function is called.

## -returns

The return value is zero if the specified time interval expired.

The return value is <b>WAIT_IO_COMPLETION</b> if the function returned due to one or more I/O completion callback functions. This can happen only if <i>bAlertable</i> is TRUE, and if the thread that called the 
<b>SleepEx</b> function is the same thread that called the extended I/O function.

## -remarks

This function causes a thread to relinquish the remainder of its time slice and become unrunnable for an interval based on the value of <i>dwMilliseconds</i>. After the sleep interval has passed, the thread is ready to run. Note that a ready thread is not guaranteed to run immediately. Consequently, the thread will not run until some arbitrary time after the sleep interval elapses, based upon the system "tick" frequency and the load factor from other processes. The system clock "ticks" at a constant rate. To increase the accuracy of the sleep interval, call the <b>timeGetDevCaps</b> function to determine the supported minimum timer resolution and the <b>timeBeginPeriod</b> function to set the timer resolution to its minimum. Use caution when calling <b>timeBeginPeriod</b>, as frequent calls can significantly affect the system clock, system power usage, and the scheduler. If you call <b>timeBeginPeriod</b>, call it one time early in the application and be sure to call the <b>timeEndPeriod</b> function at the very end of the application. If you specify 0 milliseconds, the thread will relinquish the remainder of its time slice but remain ready. For more information, see 
<a href="/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>.

This function can be used with the <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> functions to suspend a thread until an I/O operation has been completed. These functions specify a completion routine that is to be executed when the I/O operation has been completed. For the completion routine to be executed, the thread that called the I/O function must be in an alertable wait state when the completion callback function occurs. A thread goes into an alertable wait state by calling either 
<b>SleepEx</b>, 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, or 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>, with the function's <i>bAlertable</i> parameter set to TRUE.

Be careful when using <b>SleepEx</b> in the following scenarios:

<ul>
<li>Code  that directly or indirectly creates windows (for example, DDE and COM <b>CoInitialize</b>). If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. If you have a thread that uses 
<b>SleepEx</b> with infinite delay, the system will deadlock. </li>
<li>Threads that are under concurrency control. For example, an I/O completion port or thread pool limits the number of associated threads that can run. If the maximum number of threads is already running, no additional associated thread can run until a running thread finishes. If a thread uses <b>SleepEx</b> with an interval of zero to wait for one of the additional associated threads to accomplish some work,  the process might deadlock. </li>
</ul>
 For these scenarios, use 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>SleepEx</b>.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>



<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a>



<a href="/windows/desktop/ProcThread/suspending-thread-execution">Suspending Thread Execution</a>



<a href="/windows/desktop/ProcThread/multiple-threads">Threads</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitonaddress">WaitOnAddress</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
