---
UID: NF:synchapi.WaitForMultipleObjects
title: WaitForMultipleObjects function (synchapi.h)
description: Waits until one or all of the specified objects are in the signaled state or the time-out interval elapses.
helpviewer_keywords: ["WaitForMultipleObjects","WaitForMultipleObjects function","_win32_waitformultipleobjects","base.waitformultipleobjects","synchapi/WaitForMultipleObjects"]
old-location: base\waitformultipleobjects.htm
tech.root: base
ms.assetid: 51afb13c-ea7a-407a-9f21-345d84f3b96b
ms.date: 12/05/2018
ms.keywords: WaitForMultipleObjects, WaitForMultipleObjects function, _win32_waitformultipleobjects, base.waitformultipleobjects, synchapi/WaitForMultipleObjects
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
 - WaitForMultipleObjects
 - synchapi/WaitForMultipleObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Synch-L1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - WaitForMultipleObjects
---

# WaitForMultipleObjects function


## -description

Waits until one or all of the specified objects are in the signaled state or the time-out interval elapses.

To enter an alertable wait state, use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function.

## -parameters

### -param nCount [in]

The number of object handles in the array pointed to by <i>lpHandles</i>. The maximum number of object handles is <b>MAXIMUM_WAIT_OBJECTS</b>. This parameter cannot be zero.

### -param lpHandles [in]

An array of object handles. For a list of the object types whose handles can be specified, see the following Remarks section. The array can contain handles to objects of different types. It may not contain multiple copies of the same handle.

If one of these handles is closed while the wait is still pending, the function's behavior is undefined.

The handles must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>.

### -param bWaitAll [in]

If this parameter is <b>TRUE</b>, the function returns when the state of all objects in the <i>lpHandles</i> array is signaled. If <b>FALSE</b>, the function returns when the state of any one of the objects is set to signaled. In the latter case, the return value indicates the object whose state caused the function to return.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the specified objects are signaled or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the specified objects are not signaled; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the specified objects are signaled.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008, and Windows Server 2008 R2:** The <i>dwMilliseconds</i> value does include time spent in low-power states. For example, the timeout does keep counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not keep counting down while the computer is asleep.

## -returns

If the function succeeds, the return value indicates the event that caused the function to return. It can be one of the following values. (Note that <b>WAIT_OBJECT_0</b> is defined as 0 and <b>WAIT_ABANDONED_0</b> is defined as 0x00000080L.)

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_OBJECT_0</b> to (<b>WAIT_OBJECT_0</b> + <i>nCount</i>– 1)</dt>
</dl>
</td>
<td width="60%">
If <i>bWaitAll</i> is <b>TRUE</b>, a return value within the specified range indicates that the state of all specified objects is signaled. 




If <i>bWaitAll</i> is <b>FALSE</b>, the return value minus <b>WAIT_OBJECT_0</b> indicates the <i>lpHandles</i> array index of the object that satisfied the wait. If more than one object became signaled during the call, this is the array index of the signaled object with the smallest index value of all the signaled objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_ABANDONED_0</b> to (<b>WAIT_ABANDONED_0</b> + <i>nCount</i>– 1)</dt>
</dl>
</td>
<td width="60%">
If <i>bWaitAll</i> is <b>TRUE</b>, a return value within the specified range indicates that the state of all specified objects is signaled and at least one of the objects is an abandoned mutex object. 




If <i>bWaitAll</i> is <b>FALSE</b>, the return value minus [WAIT_ABANDONED_0](nf-synchapi-waitforsingleobject.md) indicates the <i>lpHandles</i> array index of an abandoned mutex object that satisfied the wait. Ownership of the mutex object is granted to the calling thread, and the mutex is set to nonsignaled.

If a mutex was protecting persistent state information, you should check it for consistency.

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
The time-out interval elapsed and the conditions specified by the <i>bWaitAll</i> parameter are not satisfied.

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

The 
<b>WaitForMultipleObjects</b> function determines whether the wait criteria have been met. If the criteria have not been met, the calling thread enters the wait state until the conditions of the wait criteria have been met or the time-out interval elapses.

When <i>bWaitAll</i> is <b>TRUE</b>, the function's wait operation is completed only when the states of all objects have been set to signaled. The function does not modify the states of the specified objects until the states of all objects have been set to signaled. For example, a mutex can be signaled, but the thread does not get ownership until the states of the other objects are also set to signaled. In the meantime, some other thread may get ownership of the mutex, thereby setting its state to nonsignaled.

When <i>bWaitAll</i> is <b>FALSE</b>, this function checks the handles in the array in order starting with index 0, until one of the objects is signaled. If multiple objects become signaled, the function returns the index of the first handle in the array whose object was signaled. 

The function modifies the state of some types of synchronization objects. Modification occurs only for the object or objects whose signaled state caused the function to return. For example, the count of a semaphore object is decreased by one. For more information, see the documentation for the individual synchronization objects.

To wait on more than <b>MAXIMUM_WAIT_OBJECTS</b> handles, use one of the following methods:

<ul>
<li>Create a thread to wait on <b>MAXIMUM_WAIT_OBJECTS</b> handles, then wait on that thread plus the other handles. Use this technique to break the handles into groups of <b>MAXIMUM_WAIT_OBJECTS</b>.</li>
<li>Call <a href="/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject">RegisterWaitForSingleObject</a> or
<a href="/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a>
to wait on each handle.
The thread pool waits efficiently on the handles and assigns a worker thread after the object is signaled or the time-out interval expires.</li>
</ul>
The 
<b>WaitForMultipleObjects</b> function can specify handles of any of the following object types in the <i>lpHandles</i> array:

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
Use caution when calling the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with no time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> function. Therefore, if you have a thread that creates windows, use 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>WaitForMultipleObjects</b>.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/waiting-for-multiple-objects">Waiting for Multiple Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject">WAIT_ABANDONED_0</a>


<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>
