---
UID: NF:synchapi.WaitForSingleObject
title: WaitForSingleObject function (synchapi.h)
description: Waits until the specified object is in the signaled state or the time-out interval elapses.
helpviewer_keywords: ["WaitForSingleObject","WaitForSingleObject function","_win32_waitforsingleobject","base.waitforsingleobject","synchapi/WaitForSingleObject","winbase/WaitForSingleObject"]
old-location: base\waitforsingleobject.htm
tech.root: base
ms.assetid: e37ebff7-b44e-469d-81ab-7a6bd1a0c822
ms.date: 12/05/2018
ms.keywords: WaitForSingleObject, WaitForSingleObject function, _win32_waitforsingleobject, base.waitforsingleobject, synchapi/WaitForSingleObject, winbase/WaitForSingleObject
req.header: synchapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
 - WaitForSingleObject
 - synchapi/WaitForSingleObject
dev_langs:
 - c++
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
 - WaitForSingleObject
---

# WaitForSingleObject function


## -description

Waits until the specified object is in the signaled state or the time-out interval elapses.

To enter an alertable wait state, use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a> function. To wait for multiple objects, use 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects">WaitForMultipleObjects</a>.

## -parameters

### -param hHandle [in]

A handle to the object. For a list of the object types whose handles can be specified, see the following Remarks section. 




If this handle is closed while the wait is still pending, the function's behavior is undefined.

The handle must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the object is signaled or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the object is not signaled; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the object is signaled.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008, and Windows Server 2008 R2:** The <i>dwMilliseconds</i> value does include time spent in low-power states. For example, the timeout does keep counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not keep counting down while the computer is asleep.

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
The specified object is a mutex object that was not released by the thread that owned the mutex object before the owning thread terminated. Ownership of the mutex object is granted to the calling thread and the mutex state is set to nonsignaled.

If the mutex was protecting persistent state information, you should check it for consistency.

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
<dt>(DWORD)0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The function has failed. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

The 
<b>WaitForSingleObject</b> function checks the current state of the specified object. If the object's state is nonsignaled, the calling thread enters the wait state until the object is signaled or the time-out interval elapses.

The function modifies the state of some types of synchronization objects. Modification occurs only for the object whose signaled state caused the function to return. For example, the count of a semaphore object is decreased by one.

The 
<b>WaitForSingleObject</b> function can wait for the following objects:

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
Use caution when calling the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with an <b>INFINITE</b> time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> function. Therefore, if you have a thread that creates windows, use 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>WaitForSingleObject</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/using-mutex-objects">Using Mutex Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>
