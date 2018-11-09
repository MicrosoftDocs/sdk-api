---
UID: NF:synchapi.WaitForSingleObjectEx
title: WaitForSingleObjectEx function
author: windows-sdk-content
description: Waits until the specified object is in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses.
old-location: base\waitforsingleobjectex.htm
tech.root: sync
ms.assetid: 530b5340-f8b2-4e00-a3ca-87a7c7372482
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: WaitForSingleObjectEx, WaitForSingleObjectEx function, _win32_waitforsingleobjectex, base.waitforsingleobjectex, synchapi/WaitForSingleObjectEx, winbase/WaitForSingleObjectEx
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
 - WaitForSingleObjectEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WaitForSingleObjectEx function


## -description


Waits until the specified object is in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses.

To wait for multiple objects, use the 
<a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>.


## -parameters




### -param hHandle [in]

A handle to the object. For a list of the object types whose handles can be specified, see the following Remarks section. 




If this handle is closed while the wait is still pending, the function's behavior is undefined.

The handle must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the object is signaled, an I/O completion routine or APC is queued, or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the criteria is not met; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the object is signaled or an I/O completion routine or APC is queued.


### -param bAlertable [in]

If this parameter is <b>TRUE</b> and the thread is in the waiting state, the function returns when the system queues an I/O completion routine or APC, and the thread runs the routine or function. Otherwise, the function does not return, and the completion routine or APC function is not executed.

A completion routine is queued when the 
<a href="base.readfileex">ReadFileEx</a> or 
<a href="base.writefileex">WriteFileEx</a> function in which it was specified has completed. The wait function returns and the completion routine is called only if <i>bAlertable</i> is <b>TRUE</b>, and the calling thread is the thread that initiated the read or write operation. An APC is queued when you call 
<a href="https://msdn.microsoft.com/5b141372-7c95-4eb2-987b-64fdf7d0783d">QueueUserAPC</a>.


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
The specified object is a mutex object that was not released by the thread that owned the mutex object before the owning thread terminated. Ownership of the mutex object is granted to the calling thread and the mutex is set to nonsignaled.

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
<a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">asynchronous procedure calls</a> (APC) queued to the thread.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WaitForSingleObjectEx</b> function determines whether the wait criteria have been met. If the criteria have not been met, the calling thread enters the wait state until the conditions of the wait criteria have been met or the time-out interval elapses.

The function modifies the state of some types of synchronization objects. Modification occurs only for the object whose signaled state caused the function to return. For example, the count of a semaphore object is decreased by one.

The 
<b>WaitForSingleObjectEx</b> function can wait for the following objects:

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
Use caution when calling the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with no time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and the <a href="_com_coinitialize">CoInitialize</a> function. Therefore, if you have a thread that creates windows, use 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> or 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>WaitForSingleObjectEx</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/8b73485c-c6f7-44df-9e53-308df2c752e7">Named Pipe Server Using Completion Routines</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>
 

 

