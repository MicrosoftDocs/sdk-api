---
UID: NF:synchapi.SetWaitableTimerEx
title: SetWaitableTimerEx function (synchapi.h)
description: Activates the specified waitable timer and provides context information for the timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.
helpviewer_keywords: ["SetWaitableTimerEx","SetWaitableTimerEx function","base.setwaitabletimerex","synchapi/SetWaitableTimerEx","winbase/SetWaitableTimerEx"]
old-location: base\setwaitabletimerex.htm
tech.root: base
ms.assetid: 2facde72-6e04-4a2f-9ee6-059f36932539
ms.date: 08/20/2024
ms.keywords: SetWaitableTimerEx, SetWaitableTimerEx function, base.setwaitabletimerex, synchapi/SetWaitableTimerEx, winbase/SetWaitableTimerEx
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - SetWaitableTimerEx
 - synchapi/SetWaitableTimerEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetWaitableTimerEx
---

# SetWaitableTimerEx function


## -description

Activates the specified waitable timer and provides context information for the timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.

## -parameters

### -param hTimer [in]

A handle to the timer object. The [CreateWaitableTimer](./nf-synchapi-createwaitabletimerexw.md) or [OpenWaitableTimer](./nf-synchapi-openwaitabletimerw.md) function returns this handle.

The handle must have the <b>TIMER_MODIFY_STATE</b> access right. For more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param lpDueTime [in]

The time after which the state of the timer is to be set to signaled, in 100 nanosecond intervals. Use the format described by the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. Positive values indicate absolute time. Be sure to use a UTC-based absolute time, as the system uses UTC-based time internally. Negative values indicate relative time. The actual timer accuracy depends on the capability of your hardware. For more information about UTC-based time, see 
<a href="/windows/desktop/SysInfo/system-time">System Time</a>.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2:** If relative time is specified, the timer includes time spent in low-power states. For example, the timer continues counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** If relative time is specified, the timer does not include time spent in low-power states. For example, the timer does not continue counting down while the computer is asleep.

### -param lPeriod [in]

The period of the timer, in milliseconds. If <i>lPeriod</i> is zero, the timer is signaled once. If <i>lPeriod</i> is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled using the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-cancelwaitabletimer">CancelWaitableTimer</a> function or reset using 
<b>SetWaitableTimerEx</b>. If <i>lPeriod</i> is less than zero, the function fails.

### -param pfnCompletionRoutine [in]

A pointer to an optional completion routine. The completion routine is application-defined function of type <b>PTIMERAPCROUTINE</b> to be executed when the timer is signaled. For more information on the timer callback function, see 
<a href="/windows/desktop/api/synchapi/nc-synchapi-ptimerapcroutine">TimerAPCProc</a>.  For more information about APCs and thread pool threads, see Remarks.

### -param lpArgToCompletionRoutine [in]

A pointer to a structure that is passed to the completion routine.

### -param WakeContext [in]

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-reason_context">REASON_CONTEXT</a> structure that contains context information for the timer.

### -param TolerableDelay [in]

The tolerable delay for expiration time, in milliseconds.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetWaitableTimerEx</b> function is similar to the <a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a> function, except <b>SetWaitableTimerEx</b> can be used to specify a context string and a tolerable delay for expiration of the timer. 

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0601 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

Timers are initially inactive. To activate a timer, call 
<b>SetWaitableTimerEx</b>. If the timer is already active when you call 
<b>SetWaitableTimerEx</b>, the timer is stopped, then it is reactivated. Stopping the timer in this manner does not set the timer state to signaled, so threads blocked in a wait operation on the timer remain blocked. However, it does cancel any pending completion routines.

When the specified due time arrives, the timer becomes inactive,
and the optional APC is queued to the thread that set the timer if there is no outstanding APC already queued.
The state of the timer is set to signaled, the timer is reactivated using the specified period, and the thread that set the timer calls the completion routine when it enters an alertable wait state.
For more information, see 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>. Note that APCs do not work as well as other signaling mechanisms  for thread pool threads because the system controls the lifetime of thread pool threads, so it is possible for a thread to be terminated before the notification is delivered. Instead of using the <i>pfnCompletionRoutine</i> parameter or another APC-based signaling mechanism, use a waitable object such as a timer created with <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer">CreateThreadpoolTimer</a>. For I/O, use  an I/O completion object created with <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a> or an <i>hEvent</i>-based <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure where the event can be passed to the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a> function.

If the thread that set the timer terminates and there is an associated completion routine, the timer is canceled. However, the state of the timer remains unchanged. If there is no completion routine, then terminating the thread has no effect on the timer.

When a manual-reset timer is set to the signaled state, it remains in this state until 
<b>SetWaitableTimerEx</b> is called to reset the timer. As a result, a periodic manual-reset timer is set to the signaled state when the initial due time arrives and remains signaled until it is reset. When a synchronization timer is set to the signaled state, it remains in this state until a thread completes a wait operation on the timer object.

If the system time is adjusted, the due time of any outstanding absolute timers is adjusted.

If the thread that called <b>SetWaitableTimerEx</b> exits, the timer is canceled. This stops the timer before it can be set to the signaled state and cancels outstanding APCs; it does not change the signaled state of the timer.

To use a timer to schedule an event for a window, use the <a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> function.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-reason_context">REASON_CONTEXT</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>
