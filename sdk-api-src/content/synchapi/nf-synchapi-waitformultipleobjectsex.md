---
UID: NF:synchapi.WaitForMultipleObjectsEx
title: WaitForMultipleObjectsEx function
author: windows-sdk-content
description: Waits until one or all of the specified objects are in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses.
old-location: base\waitformultipleobjectsex.htm
old-project: Sync
ms.assetid: 47a167fb-4714-4353-b924-a161f367673c
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: WaitForMultipleObjectsEx, WaitForMultipleObjectsEx function, _win32_waitformultipleobjectsex, base.waitformultipleobjectsex, synchapi/WaitForMultipleObjectsEx, winbase/WaitForMultipleObjectsEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - WaitForMultipleObjectsEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# WaitForMultipleObjectsEx function


## -description


Waits until one or all of the specified objects are in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses.


## -parameters




### -param nCount [in]

The number of object handles to wait for in the array pointed to by <i>lpHandles</i>. The maximum number of object handles is <b>MAXIMUM_WAIT_OBJECTS</b>. This parameter cannot be zero.


### -param lpHandles [in]

An array of object handles. For a list of the object types whose handles can be specified, see the following Remarks section. The array can contain handles of objects of different types. It may not contain multiple copies of the same handle. 




If one of these handles is closed while the wait is still pending, the function's behavior is undefined.

The handles must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.


### -param bWaitAll [in]

If this parameter is <b>TRUE</b>, the function returns when the state of all objects in the <i>lpHandles</i> array is set to signaled. If <b>FALSE</b>, the function returns when the state of any one of the objects is set to signaled. In the latter case, the return value indicates the object whose state caused the function to return.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the specified objects are signaled, an I/O completion routine or APC is queued, or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the criteria is not met; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the specified objects are signaled or an I/O completion routine or APC is queued.


### -param bAlertable [in]

If this parameter is <b>TRUE</b> and the thread is in the waiting state, the function returns when the system queues an I/O completion routine or APC, and the thread runs the routine or function. Otherwise, the function does not return and the completion routine or APC function is not executed.

A completion routine is queued when the 
<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a> or 
<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> function in which it was specified has completed. The wait function returns and the completion routine is called only if <i>bAlertable</i> is <b>TRUE</b> and the calling thread is the thread that initiated the read or write operation. An APC is queued when you call 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>.


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
If <i>bWaitAll</i> is <b>TRUE</b>, a return value in this range indicates that the state of all specified objects is signaled. 




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
If <i>bWaitAll</i> is <b>TRUE</b>, a return value in this range indicates that the state of all specified objects is signaled, and at least one of the objects is an abandoned mutex object. 




If <i>bWaitAll</i> is <b>FALSE</b>, the return value minus <b>WAIT_ABANDONED_0</b> indicates the <i>lpHandles</i> array index of an abandoned mutex object that satisfied the wait. Ownership of the mutex object is granted to the calling thread, and the mutex is set to nonsignaled.

If a mutex was protecting persistent state information, you should check it for consistency.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540625">asynchronous procedure calls</a> (APC) queued to the thread.

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
The time-out interval elapsed, the conditions specified by the <i>bWaitAll</i> parameter were not satisfied, and no completion routines are queued.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WaitForMultipleObjectsEx</b> function determines whether the wait criteria have been met. If the criteria have not been met, the calling thread enters the wait state until the conditions of the wait criteria have been met or the time-out interval elapses.

When <i>bWaitAll</i> is <b>TRUE</b>, the function's wait operation is completed only when the states of all objects have been set to signaled. The function does not modify the states of the specified objects until the states of all objects have been set to signaled. For example, a mutex can be signaled, but the thread does not get ownership until the states of the other objects are also set to signaled. In the meantime, some other thread may get ownership of the mutex, thereby setting its state to nonsignaled.

When <i>bWaitAll</i> is <b>FALSE</b>, this function checks the handles in the array in order starting with index 0, until one of the objects is signaled. If multiple objects become signaled, the function returns the index of the first handle in the array whose object was signaled.

The function modifies the state of some types of synchronization objects. Modification occurs only for the object or objects whose signaled state caused the function to return. For example, the count of a semaphore object is decreased by one. For more information, see the documentation for the individual synchronization objects.

To wait on more than <b>MAXIMUM_WAIT_OBJECTS</b> handles, use one of the following methods:

<ul>
<li>Create a thread to wait on <b>MAXIMUM_WAIT_OBJECTS</b> handles, then wait on that thread plus the other handles. Use this technique to break the handles into groups of <b>MAXIMUM_WAIT_OBJECTS</b>.</li>
<li>Call <a href="https://msdn.microsoft.com/d0cd8b28-6e20-449a-94dd-cca2be46b812">RegisterWaitForSingleObject</a> to wait on each handle. A wait thread from the thread pool waits on <b>MAXIMUM_WAIT_OBJECTS</b> registered objects and assigns a worker thread after the object is signaled or the time-out interval expires.</li>
</ul>
The 
<b>WaitForMultipleObjectsEx</b> function can specify handles of any of the following object types in the <i>lpHandles</i> array:

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
Use caution when calling the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with no time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> function. Therefore, if you have a thread that creates windows, use 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> or 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>WaitForMultipleObjectsEx</b>.




## -see-also




<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>
 

 

