---
UID: NF:synchapi.SignalObjectAndWait
title: SignalObjectAndWait function (synchapi.h)
description: Signals one object and waits on another object as a single operation.
helpviewer_keywords: ["SignalObjectAndWait","SignalObjectAndWait function","_win32_signalobjectandwait","base.signalobjectandwait","synchapi/SignalObjectAndWait"]
old-location: base\signalobjectandwait.htm
tech.root: base
ms.assetid: 2b1ce22b-8edb-4685-99f4-4fc38eec202a
ms.date: 12/05/2018
ms.keywords: SignalObjectAndWait, SignalObjectAndWait function, _win32_signalobjectandwait, base.signalobjectandwait, synchapi/SignalObjectAndWait
req.header: synchapi.h
req.include-header: Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SignalObjectAndWait
 - synchapi/SignalObjectAndWait
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SignalObjectAndWait
---

# SignalObjectAndWait function


## -description

Signals one object and waits on another object as a single operation.

## -parameters

### -param hObjectToSignal [in]

A handle to the object to be signaled. This object can be a semaphore, a mutex, or an event. 




If the handle is a semaphore, the <b>SEMAPHORE_MODIFY_STATE</b> access right is required. If the handle is an event, the <b>EVENT_MODIFY_STATE</b> access right is required. If the handle is a mutex and the caller does not own the mutex, the function fails with <b>ERROR_NOT_OWNER</b>.

### -param hObjectToWaitOn [in]

A handle to the object to wait on. The <b>SYNCHRONIZE</b> access right is required; for more information, see 
<a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>. For a list of the object types whose handles you can specify, see the Remarks section.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. The function returns if the interval elapses, even if the object's state is nonsignaled and no completion or asynchronous procedure call (APC) objects are queued. If <i>dwMilliseconds</i> is zero, the function tests the object's state, checks for queued completion routines or APCs, and returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function's time-out interval never elapses.

### -param bAlertable [in]

If this parameter is <b>TRUE</b>, the function returns when the system queues an I/O completion routine or APC function, and the thread calls the function. If <b>FALSE</b>, the function does not return, and the thread does not call the completion routine or APC function. 




A completion routine is queued when the 
function call that queued the APC has completed. This function returns and the completion routine is called only if <i>bAlertable</i> is <b>TRUE</b>, and the calling thread is the thread that queued the APC.

## -returns

If the function succeeds, the return value indicates the event that caused the function to return. It can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_ABANDONED</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
The specified object is a mutex object that was not released by the thread that owned the mutex object before the owning thread terminated. Ownership of the mutex object is granted to the calling thread, and the mutex is set to nonsignaled.

If the mutex was protecting persistent state information, you should check it for consistency.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_IO_COMPLETION</b></dt>
<dt>0x000000C0L</dt>
</dl>
</td>
<td width="60%">
The wait was ended by one or more user-mode 
<a href="/windows/desktop/Sync/asynchronous-procedure-calls">asynchronous procedure calls</a> (APC) queued to the thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_OBJECT_0</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The state of the specified object is signaled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
<dt>0x00000102L</dt>
</dl>
</td>
<td width="60%">
The time-out interval elapsed, and the object's state is nonsignaled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_FAILED</b></dt>
<dt>(<b>DWORD</b>)0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The function has failed. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

The <b>SignalObjectAndWait</b> function  provides a more efficient way to signal one object and then wait on another compared to separate function calls such as  <a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> followed by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>. 

The 
<b>SignalObjectAndWait</b> function can wait for the following objects:

<ul>
<li>Change notification</li>
<li>Console input</li>
<li>Event</li>
<li>Memory resource notification</li>
<li>Mutex</li>
<li>Process</li>
<li>Semaphore</li>
<li>Thread</li>
<li>Waitable timer</li>
</ul>
For more information, see 
<a href="/windows/desktop/Sync/synchronization-objects">Synchronization Objects</a>.

A thread can use the <b>SignalObjectAndWait</b> function to ensure that a  worker thread is in a wait state before signaling an object. For example, a thread and a worker thread may use handles to event objects to synchronize their work. The thread executes code such as the following:


``` syntax
  dwRet = WaitForSingleObject(hEventWorkerDone, INFINITE);
  if( WAIT_OBJECT_0 == dwRet)
    SetEvent(hEventMoreWorkToDo);

```

The worker thread executes code such as the following:


``` syntax
  dwRet = SignalObjectAndWait(hEventWorkerDone,
                              hEventMoreWorkToDo,
                              INFINITE, 
                              FALSE);

```

Note that the "signal" and "wait" are not guaranteed to be performed as an atomic operation. Threads executing on other processors can observe the signaled state of the first object before the thread calling <b>SignalObjectAndWait</b> begins its wait on the second object.

Use extreme caution when using  <b>SignalObjectAndWait</b>  and <a href="/windows/desktop/api/winbase/nf-winbase-pulseevent">PulseEvent</a> with Windows 7, since using these APIs among multiple threads can cause an application to deadlock. Threads that are signaled by <b>SignalObjectAndWait</b>  call <b>PulseEvent</b> to signal the waiting object of the <b>SignalObjectAndWait</b> call. In some circumstances, the caller of <b>SignalObjectAndWait</b> can't receive signal state of the waiting object in time, causing a deadlock.

Use caution when using the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with no time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and COM <b>CoInitialize</b>. Therefore, if you have a thread that creates windows, be sure to call <b>SignalObjectAndWait</b> from a different thread. If this is not possible, you can use 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, but the functionality is not equivalent.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0400 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>



<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>
