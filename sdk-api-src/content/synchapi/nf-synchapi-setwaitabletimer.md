---
UID: NF:synchapi.SetWaitableTimer
title: SetWaitableTimer function
author: windows-sdk-content
description: Activates the specified waitable timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.
old-location: base\setwaitabletimer.htm
tech.root: sync
ms.assetid: 237e22dc-696d-473f-8bb5-c28f7c7c75b2
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: SetWaitableTimer, SetWaitableTimer function, _win32_setwaitabletimer, base.setwaitabletimer, synchapi/SetWaitableTimer, winbase/SetWaitableTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: synchapi.h
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
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetWaitableTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWaitableTimer function


## -description


Activates the specified waitable timer. When the due time arrives, the timer is signaled and the thread that set the timer calls the optional completion routine.


## -parameters




### -param hTimer [in]

A handle to the timer object. The 
<a href="https://msdn.microsoft.com/41c915c4-424d-43dd-89d9-a6b4fbee701c">CreateWaitableTimer</a> or 
<a href="https://msdn.microsoft.com/0f9b49ea-5d04-449c-9b7d-f79ab28b548b">OpenWaitableTimer</a> function returns this handle. 




The handle must have the <b>TIMER_MODIFY_STATE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param lpDueTime [in]

The time after which the state of the timer is to be set to signaled, in 100 nanosecond intervals. Use the format described by the 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure. Positive values indicate absolute time. Be sure to use a UTC-based absolute time, as the system uses UTC-based time internally. Negative values indicate relative time. The actual timer accuracy depends on the capability of your hardware. For more information about UTC-based time, see 
<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>.


### -param lPeriod [in]

The period of the timer, in milliseconds. If <i>lPeriod</i> is zero, the timer is signaled once. If <i>lPeriod</i> is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled using the 
<a href="https://msdn.microsoft.com/614a237b-71b3-4091-975d-4c0b3cd6ec69">CancelWaitableTimer</a> function or reset using 
<b>SetWaitableTimer</b>. If <i>lPeriod</i> is less than zero, the function fails.


### -param pfnCompletionRoutine [in, optional]

A pointer to an optional completion routine. The completion routine is application-defined function of type <b>PTIMERAPCROUTINE</b> to be executed when the timer is signaled. For more information on the timer callback function, see 
<a href="https://msdn.microsoft.com/4e9f7bee-9c39-40d2-8588-0b3a1d7f9ede">TimerAPCProc</a>. For more information about APCs and thread pool threads, see Remarks.


### -param lpArgToCompletionRoutine [in, optional]

A pointer to a structure that is passed to the completion routine.


### -param fResume [in]

If this parameter is <b>TRUE</b>, restores a system in suspended power conservation mode when the timer state is set to signaled. Otherwise, the system is not restored. If the system does not support a restore, the call succeeds, but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_NOT_SUPPORTED</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Timers are initially inactive. To activate a timer, call 
<b>SetWaitableTimer</b>. If the timer is already active when you call 
<b>SetWaitableTimer</b>, the timer is stopped, then it is reactivated. Stopping the timer in this manner does not set the timer state to signaled, so threads blocked in a wait operation on the timer remain blocked. However, it does cancel any pending completion routines.

When the specified due time arrives, the timer becomes inactive and the optional APC is queued to the thread that set the timer. The state of the timer is set to signaled, the timer is reactivated using the specified period, and the thread that set the timer calls the completion routine when it enters an alertable wait state. If the timer is set before the thread enters an alertable wait state, the APC is canceled. For more information, see 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>. Note that APCs do not work as well as other signaling mechanisms  for thread pool threads because the system controls the lifetime of thread pool threads, so it is possible for a thread to be terminated before the notification is delivered. Instead of using the <i>pfnCompletionRoutine</i> parameter or another APC-based signaling mechanism, use a waitable object such as a timer created with <a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>. For I/O, use  an I/O completion object created with <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> or an <i>hEvent</i>-based <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure where the event can be passed to the <a href="https://msdn.microsoft.com/ebd0ecad-a864-43cf-a1cb-e4c2d595ef81">SetThreadpoolWait</a> function.

If the thread that set the timer terminates and there is an associated completion routine, the timer is canceled. However, the state of the timer remains unchanged. If there is no completion routine, then terminating the thread has no effect on the timer.

When a manual-reset timer is set to the signaled state, it remains in this state until 
<b>SetWaitableTimer</b> is called to reset the timer. As a result, a periodic manual-reset timer is set to the signaled state when the initial due time arrives and remains signaled until it is reset. When a synchronization timer is set to the signaled state, it remains in this state until a thread completes a wait operation on the timer object.

If the system time is adjusted, the due time of any outstanding absolute timers is adjusted.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

To use a timer to schedule an event for a window, use the <a href="https://msdn.microsoft.com/en-us/library/ms644906(v=VS.85).aspx">SetTimer</a> function.

APIs that deal with timers use various different hardware clocks. These clocks may have resolutions significantly different from what you expect: some may be measured in milliseconds (for those that use an RTC-based timer chip), to those measured in nanoseconds (for those that use ACPI or TSC counters). You can change the resolution of your API with a  call to the <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> and <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a> functions. How precise you can change the resolution depends on which hardware clock the particular API uses. For more information, check your hardware documentation. 


#### Examples

For an example that uses 
<b>SetWaitableTimer</b>, see 
<a href="https://msdn.microsoft.com/3c84c2ad-6bac-4f14-a633-51d4529314af">Using Waitable Timer Objects</a>.


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/614a237b-71b3-4091-975d-4c0b3cd6ec69">CancelWaitableTimer</a>



<a href="https://msdn.microsoft.com/41c915c4-424d-43dd-89d9-a6b4fbee701c">CreateWaitableTimer</a>



<a href="https://msdn.microsoft.com/0f9b49ea-5d04-449c-9b7d-f79ab28b548b">OpenWaitableTimer</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/4e9f7bee-9c39-40d2-8588-0b3a1d7f9ede">TimerAPCProc</a>



<a href="https://msdn.microsoft.com/5d39ada0-ea31-40d7-b075-aeb657ee508c">Waitable Timer Objects</a>
 

 

