---
UID: NF:synchapi.SetWaitableTimerEx
title: SetWaitableTimerEx function
author: windows-sdk-content
description: Activates the specified waitable timer and provides context information for the timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.
old-location: base\setwaitabletimerex.htm
old-project: Sync
ms.assetid: 2facde72-6e04-4a2f-9ee6-059f36932539
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SetWaitableTimerEx, SetWaitableTimerEx function, base.setwaitabletimerex, synchapi/SetWaitableTimerEx, winbase/SetWaitableTimerEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - kernel32.dll
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetWaitableTimerEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# SetWaitableTimerEx function


## -description


Activates the specified waitable timer and provides context information for the timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.


## -parameters




### -param hTimer [in]

A handle to the timer object. The <a href="https://msdn.microsoft.com/9ef51567-7d0f-4a2e-a798-289564733410">CreateWaitableTimer</a> or <a href="https://msdn.microsoft.com/0f9b49ea-5d04-449c-9b7d-f79ab28b548b">OpenWaitableTimer</a> function returns this handle.

The handle must have the <b>TIMER_MODIFY_STATE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param lpDueTime [in]

The time after which the state of the timer is to be set to signaled, in 100 nanosecond intervals. Use the format described by the 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure. Positive values indicate absolute time. Be sure to use a UTC-based absolute time, as the system uses UTC-based time internally. Negative values indicate relative time. The actual timer accuracy depends on the capability of your hardware. For more information about UTC-based time, see 
<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>.


### -param lPeriod [in]

The period of the timer, in milliseconds. If <i>lPeriod</i> is zero, the timer is signaled once. If <i>lPeriod</i> is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled using the 
<a href="https://msdn.microsoft.com/614a237b-71b3-4091-975d-4c0b3cd6ec69">CancelWaitableTimer</a> function or reset using 
<b>SetWaitableTimerEx</b>. If <i>lPeriod</i> is less than zero, the function fails.


### -param pfnCompletionRoutine [in]

A pointer to an optional completion routine. The completion routine is application-defined function of type <b>PTIMERAPCROUTINE</b> to be executed when the timer is signaled. For more information on the timer callback function, see 
<a href="https://msdn.microsoft.com/4e9f7bee-9c39-40d2-8588-0b3a1d7f9ede">TimerAPCProc</a>.  For more information about APCs and thread pool threads, see Remarks.


### -param lpArgToCompletionRoutine [in]

A pointer to a structure that is passed to the completion routine.


### -param WakeContext [in]

Pointer to a <a href="https://msdn.microsoft.com/006bb84f-5e51-4f6e-8a44-6b50e763c5ca">REASON_CONTEXT</a> structure that contains context information for the timer. 


### -param TolerableDelay [in]

The tolerable delay for expiration time, in milliseconds.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>SetWaitableTimerEx</b> function is similar to the <a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a> function, except <b>SetWaitableTimerEx</b> can be used to specify a context string and a tolerable delay for expiration of the timer. 

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0601 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

Timers are initially inactive. To activate a timer, call 
<b>SetWaitableTimerEx</b>. If the timer is already active when you call 
<b>SetWaitableTimerEx</b>, the timer is stopped, then it is reactivated. Stopping the timer in this manner does not set the timer state to signaled, so threads blocked in a wait operation on the timer remain blocked. However, it does cancel any pending completion routines.

When the specified due time arrives, the timer becomes inactive and the optional APC is queued to the thread that set the timer. The state of the timer is set to signaled, the timer is reactivated using the specified period, and the thread that set the timer calls the completion routine when it enters an alertable wait state. If the timer is set before the thread enters an alertable wait state, the APC is canceled. For more information, see 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>. Note that APCs do not work as well as other signaling mechanisms  for thread pool threads because the system controls the lifetime of thread pool threads, so it is possible for a thread to be terminated before the notification is delivered. Instead of using the <i>pfnCompletionRoutine</i> parameter or another APC-based signaling mechanism, use a waitable object such as a timer created with <a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>. For I/O, use  an I/O completion object created with <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> or an <i>hEvent</i>-based <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure where the event can be passed to the <a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a> function.

If the thread that set the timer terminates and there is an associated completion routine, the timer is canceled. However, the state of the timer remains unchanged. If there is no completion routine, then terminating the thread has no effect on the timer.

When a manual-reset timer is set to the signaled state, it remains in this state until 
<b>SetWaitableTimerEx</b> is called to reset the timer. As a result, a periodic manual-reset timer is set to the signaled state when the initial due time arrives and remains signaled until it is reset. When a synchronization timer is set to the signaled state, it remains in this state until a thread completes a wait operation on the timer object.

If the system time is adjusted, the due time of any outstanding absolute timers is adjusted.

If the thread that called <b>SetWaitableTimerEx</b> exits, the timer is canceled. This stops the timer before it can be set to the signaled state and cancels outstanding APCs; it does not change the signaled state of the timer.

To use a timer to schedule an event for a window, use the <a href="https://msdn.microsoft.com/library/ms644906(v=VS.85).aspx">SetTimer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/006bb84f-5e51-4f6e-8a44-6b50e763c5ca">REASON_CONTEXT</a>



<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>
 

 

