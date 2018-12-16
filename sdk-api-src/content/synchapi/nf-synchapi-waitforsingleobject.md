---
UID: NF:synchapi.WaitForSingleObject
title: WaitForSingleObject function
author: windows-sdk-content
description: Waits until the specified object is in the signaled state or the time-out interval elapses.
old-location: base\waitforsingleobject.htm
tech.root: sync
ms.assetid: e37ebff7-b44e-469d-81ab-7a6bd1a0c822
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WaitForSingleObject, WaitForSingleObject function, _win32_waitforsingleobject, base.waitforsingleobject, synchapi/WaitForSingleObject, winbase/WaitForSingleObject
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
 - WaitForSingleObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WaitForSingleObject function


## -description


Waits until the specified object is in the signaled state or the time-out interval elapses.

To enter an alertable wait state, use the 
<a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a> function. To wait for multiple objects, use 
<a href="https://msdn.microsoft.com/51afb13c-ea7a-407a-9f21-345d84f3b96b">WaitForMultipleObjects</a>.


## -parameters




### -param hHandle [in]

A handle to the object. For a list of the object types whose handles can be specified, see the following Remarks section. 




If this handle is closed while the wait is still pending, the function's behavior is undefined.

The handle must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the object is signaled or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the object is not signaled; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the object is signaled.

<b>Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2:  </b>The <i>dwMilliseconds</i> value does include time spent in low-power states. For example, the timeout does keep counting down while the computer is asleep.

<b>Windows 8, Windows Server 2012, Windows 8.1, Windows Server 2012 R2, Windows 10 and Windows Server 2016:  </b>The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not keep counting down while the computer is asleep.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
Use caution when calling the wait functions and code that directly or indirectly creates windows. If a thread creates any windows, it must process messages. Message broadcasts are sent to all windows in the system. A thread that uses a wait function with no time-out interval may cause the system to become deadlocked. Two examples of code that indirectly creates windows are DDE and the <a href="https://msdn.microsoft.com/en-us/library/ms678543(v=VS.85).aspx">CoInitialize</a> function. Therefore, if you have a thread that creates windows, use 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> or 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, rather than 
<b>WaitForSingleObject</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0f69ba50-69ce-467a-b068-8fd8f07c6c78">Using Mutex Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>
 

 

