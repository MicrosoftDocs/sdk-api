---
UID: NF:winuser.MsgWaitForMultipleObjects
title: MsgWaitForMultipleObjects function
author: windows-sdk-content
description: Waits until one or all of the specified objects are in the signaled state or the time-out interval elapses. The objects can include input event objects.
old-location: base\msgwaitformultipleobjects.htm
tech.root: sync
ms.assetid: 0629f1b3-6805-43a7-9aeb-4f80939ec62c
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: MsgWaitForMultipleObjects, MsgWaitForMultipleObjects function, QS_ALLEVENTS, QS_ALLINPUT, QS_ALLPOSTMESSAGE, QS_HOTKEY, QS_INPUT, QS_KEY, QS_MOUSE, QS_MOUSEBUTTON, QS_MOUSEMOVE, QS_PAINT, QS_POSTMESSAGE, QS_RAWINPUT, QS_SENDMESSAGE, QS_TIMER, _win32_msgwaitformultipleobjects, base.msgwaitformultipleobjects, winuser/MsgWaitForMultipleObjects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Message-l1-1-0.dll
 - IE_Shims.dll
 - API-MS-Win-RTCore-NTUser-synch-l1-1-0.dll
 - MinUser.dll
 - Ext-MS-Win-NTUser-synch-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-synch-Ext-l1-1-0.dll
 - NTUserSynchExtHost.dll
 - ComBase.dll
api_name:
 - MsgWaitForMultipleObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsgWaitForMultipleObjects function


## -description


Waits until one or all of the specified objects are in the signaled state or the time-out interval elapses. The objects can include input event objects, which you specify using the <i>dwWakeMask</i> parameter.

To enter an alertable wait state, use the 
<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a> function.


## -parameters




### -param nCount [in]

The number of object handles in the array pointed to by <i>pHandles</i>. The maximum number of object handles is <b>MAXIMUM_WAIT_OBJECTS</b> minus one. If this parameter has the value zero, then the function waits only for an input event.


### -param pHandles [in]

An array of object handles. For a list of the object types whose handles can be specified, see the following Remarks section. The array can contain handles of objects of different types. It may not contain multiple copies of the same handle. 




If one of these handles is closed while the wait is still pending, the function's behavior is undefined.

The handles must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">Standard Access Rights</a>.


### -param fWaitAll [in]

If this parameter is <b>TRUE</b>, the function returns when the states of all objects in the <i>pHandles</i> array have been set to signaled and an input event has been received. If this parameter is <b>FALSE</b>, the function returns when the state of any one of the objects is set to signaled or an input event has been received. In this case, the return value indicates the object whose state caused the function to return.


### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the specified objects are signaled or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the specified objects are not signaled; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the specified objects are signaled.


### -param dwWakeMask [in]

The input types for which an input event object handle will be added to the array of object handles. This parameter can be any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QS_ALLEVENTS"></a><a id="qs_allevents"></a><dl>
<dt><b>QS_ALLEVENTS</b></dt>
<dt>0x04BF</dt>
</dl>
</td>
<td width="60%">
An input, <a href="_win32_WM_TIMER_cpp">WM_TIMER</a>, <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>, <a href="_win32_WM_HOTKEY_cpp">WM_HOTKEY</a>, or posted message is in the queue.

This value is a combination of <b>QS_INPUT</b>, <b>QS_POSTMESSAGE</b>, <b>QS_TIMER</b>, <b>QS_PAINT</b>, and <b>QS_HOTKEY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_ALLINPUT"></a><a id="qs_allinput"></a><dl>
<dt><b>QS_ALLINPUT</b></dt>
<dt>0x04FF</dt>
</dl>
</td>
<td width="60%">
Any message is in the queue.

This value is a combination of <b>QS_INPUT</b>, <b>QS_POSTMESSAGE</b>, <b>QS_TIMER</b>, <b>QS_PAINT</b>, <b>QS_HOTKEY</b>, and <b>QS_SENDMESSAGE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_ALLPOSTMESSAGE"></a><a id="qs_allpostmessage"></a><dl>
<dt><b>QS_ALLPOSTMESSAGE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
A posted message is in the queue.

This value is cleared when you call <a href="_win32_getmessage_cpp">GetMessage</a> or <a href="_win32_peekmessage_cpp">PeekMessage</a> without filtering messages.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_HOTKEY"></a><a id="qs_hotkey"></a><dl>
<dt><b>QS_HOTKEY</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
A <a href="_win32_WM_HOTKEY_cpp">WM_HOTKEY</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_INPUT"></a><a id="qs_input"></a><dl>
<dt><b>QS_INPUT</b></dt>
<dt>0x407</dt>
</dl>
</td>
<td width="60%">
An input message is in the queue.

This value is a combination of <b>QS_MOUSE</b>, <b>QS_KEY</b>, and 
         <b>QS_RAWINPUT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_KEY"></a><a id="qs_key"></a><dl>
<dt><b>QS_KEY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A <a href="_win32_WM_KEYUP_cpp">WM_KEYUP</a>, <a href="_win32_WM_KEYDOWN_cpp">WM_KEYDOWN</a>, <a href="_win32_WM_SYSKEYUP_cpp">WM_SYSKEYUP</a>, or <a href="_win32_WM_SYSKEYDOWN_cpp">WM_SYSKEYDOWN</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSE"></a><a id="qs_mouse"></a><dl>
<dt><b>QS_MOUSE</b></dt>
<dt>0x0006</dt>
</dl>
</td>
<td width="60%">
A <a href="_win32_WM_MOUSEMOVE_cpp">WM_MOUSEMOVE</a> message or mouse-button message (<b>WM_LBUTTONUP</b>, <a href="_win32_WM_RBUTTONDOWN_cpp">WM_RBUTTONDOWN</a>, and so on).

This value is a combination of <b>QS_MOUSEMOVE</b> and <b>QS_MOUSEBUTTON</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEBUTTON"></a><a id="qs_mousebutton"></a><dl>
<dt><b>QS_MOUSEBUTTON</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
A mouse-button message (<b>WM_LBUTTONUP</b>, <a href="_win32_WM_RBUTTONDOWN_cpp">WM_RBUTTONDOWN</a>, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="QS_MOUSEMOVE"></a><a id="qs_mousemove"></a><dl>
<dt><b>QS_MOUSEMOVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A <a href="_win32_WM_MOUSEMOVE_cpp">WM_MOUSEMOVE</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_PAINT"></a><a id="qs_paint"></a><dl>
<dt><b>QS_PAINT</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_POSTMESSAGE"></a><a id="qs_postmessage"></a><dl>
<dt><b>QS_POSTMESSAGE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
A posted message is in the queue.

This value is cleared when you call <a href="_win32_getmessage_cpp">GetMessage</a> or <a href="_win32_peekmessage_cpp">PeekMessage</a>, whether or not you are filtering messages.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_RAWINPUT"></a><a id="qs_rawinput"></a><dl>
<dt><b>QS_RAWINPUT</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
 A raw input message is in the queue. For more information, see 
<a href="_win32_raw_input_cpp">Raw Input</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_SENDMESSAGE"></a><a id="qs_sendmessage"></a><dl>
<dt><b>QS_SENDMESSAGE</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
A message sent by another thread or application is in the queue.

</td>
</tr>
<tr>
<td width="40%"><a id="QS_TIMER"></a><a id="qs_timer"></a><dl>
<dt><b>QS_TIMER</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
A <a href="_win32_WM_TIMER_cpp">WM_TIMER</a> message is in the queue.

</td>
</tr>
</table>
 


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
<dt><b>WAIT_OBJECT_0</b> to
(<b>WAIT_OBJECT_0</b> + <i>nCount</i>– 1)</dt>
</dl>
</td>
<td width="60%">
If <i>bWaitAll</i> is <b>TRUE</b>, the return value indicates that the state of all specified objects is signaled. If <i>bWaitAll</i> is <b>FALSE</b>, the return value minus <b>WAIT_OBJECT_0</b> indicates the <i>pHandles</i> array index of the object that satisfied the wait.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_OBJECT_0</b> + <i>nCount</i></dt>
</dl>
</td>
<td width="60%">
New input of the type specified in the <i>dwWakeMask</i> parameter is available in the thread's input queue. Functions such as 
<a href="_win32_peekmessage_cpp">PeekMessage</a>, 
<a href="_win32_getmessage_cpp">GetMessage</a>, and 
<a href="_win32_waitmessage_cpp">WaitMessage</a> mark messages in the queue as old messages. Therefore, after you call one of these functions, a subsequent call to 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> will not return until new input of the specified type arrives. 




This value is also returned upon the occurrence of a system event that requires the thread's action, such as foreground activation. Therefore, 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a> can return even though no appropriate input is available and even if <i>dwWakeMask</i> is set to 0. If this occurs, call <a href="_win32_getmessage_cpp">GetMessage</a> or <a href="_win32_peekmessage_cpp">PeekMessage</a> to process the system event before trying the call to 
<b>MsgWaitForMultipleObjects</b> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_ABANDONED_0</b> to
(<b>WAIT_ABANDONED_0</b> + <i>nCount</i>– 1)</dt>
</dl>
</td>
<td width="60%">
If <i>bWaitAll</i> is <b>TRUE</b>, the return value indicates that the state of all specified objects is signaled and at least one of the objects is an abandoned mutex object. If <i>bWaitAll</i> is <b>FALSE</b>, the return value minus <b>WAIT_ABANDONED_0</b> indicates the <i>pHandles</i> array index of an abandoned mutex object that satisfied the wait. Ownership of the mutex object is granted to the calling thread, and the mutex is set to nonsignaled.

If the mutex was protecting persistent state information, you should check it for consistency.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
<dt>258L</dt>
</dl>
</td>
<td width="60%">
The time-out interval elapsed and the conditions specified by the <i>bWaitAll</i> and <i>dwWakeMask</i> parameters were not satisfied.

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
<b>MsgWaitForMultipleObjects</b> function determines whether the wait criteria have been met. If the criteria have not been met, the calling thread enters the wait state until the conditions of the wait criteria have been met or the time-out interval elapses.

When <i>bWaitAll</i> is <b>TRUE</b>, the function does not modify the states of the specified objects until the states of all objects have been set to signaled. For example, a mutex can be signaled, but the thread does not get ownership until the states of the other objects have also been set to signaled. In the meantime, some other thread may get ownership of the mutex, thereby setting its state to nonsignaled.

When <i>bWaitAll</i> is <b>TRUE</b>, the function's wait is completed only when the states of all objects have been set to signaled and an input event has been received. Therefore, setting <i>bWaitAll</i> to <b>TRUE</b> prevents input from being processed until the state of all objects in the <i>pHandles</i> array have been set to signaled. For this reason, if you set <i>bWaitAll</i> to <b>TRUE</b>, you should use a short timeout value in <i>dwMilliseconds</i>. If you have a thread that creates windows waiting for all objects in the <i>pHandles</i> array, including input events specified by <i>dwWakeMask</i>, with no timeout interval, the system will deadlock. This is because threads that create windows must process messages. DDE sends message to all windows in the system. Therefore, if a thread creates windows, do not set the <i>bWaitAll</i> parameter to <b>TRUE</b> in calls to 
<b>MsgWaitForMultipleObjects</b> made from that thread.

When <i>bWaitAll</i> is <b>FALSE</b>, this function checks the handles in the array in order starting with index 0, until one of the objects is signaled. If multiple objects become signaled, the function returns the index of the first handle in the array whose object was signaled.

<b>MsgWaitForMultipleObjects</b> does not return if there is unread input of the specified type in the message queue after the thread has called a function to check the queue. This is because functions such as 
<a href="_win32_peekmessage_cpp">PeekMessage</a>, 
<a href="_win32_getmessage_cpp">GetMessage</a>, 
<a href="_win32_getqueuestatus_cpp">GetQueueStatus</a>, and 
<a href="_win32_waitmessage_cpp">WaitMessage</a> check the queue and then change the state information for the queue so that the input is no longer considered new. A subsequent call to 
<b>MsgWaitForMultipleObjects</b> will not return until new input of the specified type arrives. The existing unread input (received prior to the last time the thread checked the queue) is ignored.

The function modifies the state of some types of synchronization objects. Modification occurs only for the object or objects whose signaled state caused the function to return. For example, the count of a semaphore object is decreased by one. For more information, see the documentation for the individual synchronization objects.

The 
<b>MsgWaitForMultipleObjects</b> function can specify handles of any of the following object types in the <i>pHandles</i> array:

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
The <b>QS_ALLPOSTMESSAGE</b> and <b>QS_POSTMESSAGE</b> flags differ in when they are cleared. <b>QS_POSTMESSAGE</b> is cleared when you call <a href="_win32_getmessage_cpp">GetMessage</a> or <a href="_win32_peekmessage_cpp">PeekMessage</a>, whether or not you are filtering messages. <b>QS_ALLPOSTMESSAGE</b> is cleared when you call <b>GetMessage</b> or <a href="_win32_peekmessage_cpp">PeekMessage</a> without filtering messages (<i>wMsgFilterMin</i> and <i>wMsgFilterMax</i> are 0). This can be useful when you call <a href="_win32_peekmessage_cpp">PeekMessage</a> multiple times to get messages in different ranges.




## -see-also




<a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>
 

 

