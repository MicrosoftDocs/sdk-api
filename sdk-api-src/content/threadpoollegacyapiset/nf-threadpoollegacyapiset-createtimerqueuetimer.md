---
UID: NF:threadpoollegacyapiset.CreateTimerQueueTimer
title: CreateTimerQueueTimer function (threadpoollegacyapiset.h)
description: Creates a timer-queue timer. This timer expires at the specified due time, then after every specified period. When the timer expires, the callback function is called.
helpviewer_keywords: ["CreateTimerQueueTimer","CreateTimerQueueTimer function","WT_EXECUTEDEFAULT","WT_EXECUTEINIOTHREAD","WT_EXECUTEINPERSISTENTTHREAD","WT_EXECUTEINTIMERTHREAD","WT_EXECUTELONGFUNCTION","WT_EXECUTEONLYONCE","WT_TRANSFER_IMPERSONATION","_win32_createtimerqueuetimer","base.createtimerqueuetimer","threadpoollegacyapiset/CreateTimerQueueTimer","winbase/CreateTimerQueueTimer"]
old-location: base\createtimerqueuetimer.htm
tech.root: backup
ms.assetid: dfcbea5c-e2b7-40e4-b1a2-3cc7446d8844
ms.date: 12/05/2018
ms.keywords: CreateTimerQueueTimer, CreateTimerQueueTimer function, WT_EXECUTEDEFAULT, WT_EXECUTEINIOTHREAD, WT_EXECUTEINPERSISTENTTHREAD, WT_EXECUTEINTIMERTHREAD, WT_EXECUTELONGFUNCTION, WT_EXECUTEONLYONCE, WT_TRANSFER_IMPERSONATION, _win32_createtimerqueuetimer, base.createtimerqueuetimer, threadpoollegacyapiset/CreateTimerQueueTimer, winbase/CreateTimerQueueTimer
req.header: threadpoollegacyapiset.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CreateTimerQueueTimer
 - threadpoollegacyapiset/CreateTimerQueueTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateTimerQueueTimer
---

# CreateTimerQueueTimer function


## -description

Creates a timer-queue timer. This timer expires at the specified due time, then after every specified period. When the timer expires, the callback function is called.

## -parameters

### -param phNewTimer [out]

A pointer to a buffer that receives a handle to the timer-queue timer on return. When this handle has expired and is no longer required, release it by calling <a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>.

### -param TimerQueue [in, optional]

A handle to the timer queue. This handle is returned by the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a> function.

If this parameter is <b>NULL</b>, the timer is associated with the default timer queue.

### -param Callback [in]

A pointer to the application-defined function of type <b>WAITORTIMERCALLBACK</b> to be executed when the timer expires. For more information, see 
<a href="/previous-versions/windows/desktop/legacy/ms687066(v=vs.85)">WaitOrTimerCallback</a>.

### -param Parameter [in, optional]

A single parameter value that will be passed to the callback function.

### -param DueTime [in]

The amount of time in milliseconds relative to the current time that must elapse before the timer is signaled for the first time.

### -param Period [in]

The period of the timer, in milliseconds. If this parameter is zero, the timer is signaled once. If this parameter is greater than zero, the timer is periodic. A periodic timer automatically reactivates each time the period elapses, until the timer is canceled.

### -param Flags [in]

This parameter can be one or more of the following values from WinNT.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEDEFAULT"></a><a id="wt_executedefault"></a><dl>
<dt><b>WT_EXECUTEDEFAULT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
By default, the callback function is queued to a non-I/O worker thread.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEINTIMERTHREAD"></a><a id="wt_executeintimerthread"></a><dl>
<dt><b>WT_EXECUTEINTIMERTHREAD</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The callback function is invoked by the timer thread itself. This flag should be used only for short tasks or it could affect other timer operations. 




The callback function is queued as an APC. It should not perform alertable wait operations.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEINIOTHREAD"></a><a id="wt_executeiniothread"></a><dl>
<dt><b>WT_EXECUTEINIOTHREAD</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This flag is not used.

<b>Windows Server 2003 and Windows XP:  </b>The callback function is queued to an I/O worker thread. This flag should be used if the function should be executed in a thread that waits in an alertable state. 


I/O worker threads were removed starting with Windows Vista and Windows Server 2008.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEINPERSISTENTTHREAD"></a><a id="wt_executeinpersistentthread"></a><dl>
<dt><b>WT_EXECUTEINPERSISTENTTHREAD</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The callback function is queued to a thread that never terminates. It does not guarantee that the same thread is used each time. This flag should be used only for short tasks or it could affect other timer operations. 


This flag must be set if the thread calls functions that use APCs. For more information, see <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.

Note that currently no worker thread is truly persistent, although no worker thread will terminate if there are any pending I/O requests.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTELONGFUNCTION"></a><a id="wt_executelongfunction"></a><dl>
<dt><b>WT_EXECUTELONGFUNCTION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The callback function can perform a long wait. This flag helps the system to decide if it should create a new thread.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_EXECUTEONLYONCE"></a><a id="wt_executeonlyonce"></a><dl>
<dt><b>WT_EXECUTEONLYONCE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The timer will be set to the signaled state only once. If this flag is set, the <i>Period</i> parameter must be zero.

</td>
</tr>
<tr>
<td width="40%"><a id="WT_TRANSFER_IMPERSONATION"></a><a id="wt_transfer_impersonation"></a><dl>
<dt><b>WT_TRANSFER_IMPERSONATION</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Callback functions will use the current access token, whether it is a process or impersonation token. If this flag is not specified, callback functions execute only with the process token.

<b>Windows XP:  </b>This flag is not supported until Windows XP with SP2 and Windows Server 2003.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>DueTime</i> and <i>Period</i> parameters are both nonzero, the timer will be signaled first at the due time, then periodically. The callback is called every time the period elapses, whether or not the previous callback has finished executing. Callback functions are queued to the thread pool. These threads are subject to scheduling delays, so the timing can vary depending on what else is happening in the application or the system.

The time that the system spends in sleep or hibernation does not count toward the expiration of the timer. The timer is signaled when the cumulative amount of elapsed time the system spends in the waking state matches the timer's due time or period. 

<b>Windows Server 2003 and Windows XP:  </b>The time that the system spends in sleep or hibernation counts toward the expiration of the timer.  If the timer expires while the system is sleeping, the timer is signaled immediately when the system wakes.

To cancel a timer, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a> function. To cancel all timers in a timer queue, call the 
<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a> function.

By default, the thread pool has a maximum of 500 threads. To raise this limit, use the <b>WT_SET_MAX_THREADPOOL_THREAD</b> macro defined in WinNT.h.


``` syntax
#define WT_SET_MAX_THREADPOOL_THREADS(Flags,Limit) \
    ((Flags)|=(Limit)<<16)
```

Use this macro when specifying the <i>Flags</i> parameter. The macro parameters are the desired flags and the new limit (up to (2&lt;&lt;16)-1 threads). However, note that your application can improve its performance by keeping the number of worker threads low.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example that uses 
<b>CreateTimerQueueTimer</b>, see 
<a href="/windows/desktop/Sync/using-timer-queues">Using Timer Queues</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex">DeleteTimerQueueEx</a>



<a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer">DeleteTimerQueueTimer</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>



<a href="/windows/desktop/Sync/timer-queues">Timer Queues</a>
