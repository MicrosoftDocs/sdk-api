---
UID: NF:winuser.MsgWaitForMultipleObjectsEx
title: MsgWaitForMultipleObjectsEx function (winuser.h)
description: Waits until one or all of the specified objects are in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses. The array of objects can include input event objects.
helpviewer_keywords: ["MWMO_ALERTABLE","MWMO_INPUTAVAILABLE","MWMO_WAITALL","MsgWaitForMultipleObjectsEx","MsgWaitForMultipleObjectsEx function","QS_ALLEVENTS","QS_ALLINPUT","QS_ALLPOSTMESSAGE","QS_HOTKEY","QS_INPUT","QS_KEY","QS_MOUSE","QS_MOUSEBUTTON","QS_MOUSEMOVE","QS_PAINT","QS_POSTMESSAGE","QS_RAWINPUT","QS_SENDMESSAGE","QS_TIMER","_win32_msgwaitformultipleobjectsex","base.msgwaitformultipleobjectsex","winuser/MsgWaitForMultipleObjectsEx"]
old-location: base\msgwaitformultipleobjectsex.htm
tech.root: backup
ms.assetid: 1774b721-3ad4-492e-96af-b71de9066f0c
ms.date: 12/05/2018
ms.keywords: MWMO_ALERTABLE, MWMO_INPUTAVAILABLE, MWMO_WAITALL, MsgWaitForMultipleObjectsEx, MsgWaitForMultipleObjectsEx function, QS_ALLEVENTS, QS_ALLINPUT, QS_ALLPOSTMESSAGE, QS_HOTKEY, QS_INPUT, QS_KEY, QS_MOUSE, QS_MOUSEBUTTON, QS_MOUSEMOVE, QS_PAINT, QS_POSTMESSAGE, QS_RAWINPUT, QS_SENDMESSAGE, QS_TIMER, _win32_msgwaitformultipleobjectsex, base.msgwaitformultipleobjectsex, winuser/MsgWaitForMultipleObjectsEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsgWaitForMultipleObjectsEx
 - winuser/MsgWaitForMultipleObjectsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Message-l1-1-0.dll
 - IE_Shims.dll
 - API-MS-Win-RTCore-NTUser-Synch-l1-1-0.dll
 - MinUser.dll
 - Ext-MS-Win-NTUser-Synch-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-synch-Ext-l1-1-0.dll
 - NTUserSynchExtHost.dll
 - ComBase.dll
api_name:
 - MsgWaitForMultipleObjectsEx
---

# MsgWaitForMultipleObjectsEx function


## -description

Waits until one or all of the specified objects are in the signaled state, an I/O completion routine or asynchronous procedure call (APC) is queued to the thread, or the time-out interval elapses. The array of objects can include input event objects, which you specify using the <i>dwWakeMask</i> parameter.

## -parameters

### -param nCount [in]

The number of object handles in the array pointed to by <i>pHandles</i>. The maximum number of object handles is <b>MAXIMUM_WAIT_OBJECTS</b> minus one. If this parameter has the value zero, then the function waits only for an input event.

### -param pHandles [in]

An array of object handles. For a list of the object types whose handles you can specify, see the Remarks section later in this topic. The array can contain handles to multiple types of objects. It may not contain multiple copies of the same handle. 




If one of these handles is closed while the wait is still pending, the function's behavior is undefined.

The handles must have the <b>SYNCHRONIZE</b> access right. For more information, see 
<a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If a nonzero value is specified, the function waits until the specified objects are signaled, an I/O completion routine or APC is queued, or the interval elapses. If <i>dwMilliseconds</i> is zero, the function does not enter a wait state if the criteria is not met; it always returns immediately. If <i>dwMilliseconds</i> is <b>INFINITE</b>, the function will return only when the specified objects are signaled or an I/O completion routine or APC is queued.

**Windows XP, Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008, and Windows Server 2008 R2:** The <i>dwMilliseconds</i> value does include time spent in low-power states. For example, the timeout does keep counting down while the computer is asleep.

**Windows 8 and newer, Windows Server 2012 and newer:** The <i>dwMilliseconds</i> value does not include time spent in low-power states. For example, the timeout does not keep counting down while the computer is asleep.

### -param dwWakeMask [in]

The input types for which an input event object handle will be added to the array of object handles. This parameter can be any combination of the values listed in [GetQueueStatus](/windows/win32/api/winuser/nf-winuser-getqueuestatus) *flags* parameter.

### -param dwFlags [in]

The wait type. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The function returns when any one of the objects is signaled. The return value indicates the object whose state caused the function to return.

</td>
</tr>
<tr>
<td width="40%"><a id="MWMO_ALERTABLE"></a><a id="mwmo_alertable"></a><dl>
<dt><b>MWMO_ALERTABLE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The function also returns if an APC has been queued to the thread with 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a> while the thread is in the waiting state.

</td>
</tr>
<tr>
<td width="40%"><a id="MWMO_INPUTAVAILABLE"></a><a id="mwmo_inputavailable"></a><dl>
<dt><b>MWMO_INPUTAVAILABLE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The function returns if input exists for the queue, even if the input has been seen (but not removed) using a call to another function, such as 
<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MWMO_WAITALL"></a><a id="mwmo_waitall"></a><dl>
<dt><b>MWMO_WAITALL</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The function returns when all objects in the <i>pHandles</i> array are signaled and an input event has been received, all at the same time.

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
 (<b>WAIT_OBJECT_0</b> + <i>nCount</i> - 1)</dt>
</dl>
</td>
<td width="60%">
If the <b>MWMO_WAITALL</b> flag is used, a return value within the specified range indicates that the state of all specified objects is signaled. Otherwise, the return value minus <b>WAIT_OBJECT_0</b> indicates the <i>pHandles</i> array index of the object that caused the function to return.

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
<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, 
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>, 
<a href="/windows/desktop/direct3d10/id3dx10threadpump-getqueuestatus">GetQueueStatus</a>, and 
<a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a> mark messages in the queue as old messages. Therefore, after you call one of these functions, a subsequent call to 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> will not return until new input of the specified type arrives. 




This value is also returned upon the occurrence of a system event that requires the thread's action, such as foreground activation. Therefore, 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> can return even though no appropriate input is available and even if <i>dwWakeMask</i> is set to 0. If this occurs, call <a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> to process the system event before trying the call to 
<b>MsgWaitForMultipleObjectsEx</b> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_ABANDONED_0</b> to
(<b>WAIT_ABANDONED_0</b> + <i>nCount</i> - 1)</dt>
</dl>
</td>
<td width="60%">
If the <b>MWMO_WAITALL</b> flag is used, a return value within the specified range indicates that the state of all specified objects is signaled and at least one of the objects is an abandoned mutex object. Otherwise, the return value minus <b>WAIT_ABANDONED_0</b> indicates the <i>pHandles</i> array index of an abandoned mutex object that caused the function to return. Ownership of the mutex object is granted to the calling thread, and the mutex is set to nonsignaled.

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
<dt><b>WAIT_TIMEOUT</b></dt>
<dt>258L</dt>
</dl>
</td>
<td width="60%">
The time-out interval elapsed, but the conditions specified by the <i>dwFlags</i> and <i>dwWakeMask</i> parameters were not met.

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
<b>MsgWaitForMultipleObjectsEx</b> function determines whether the conditions specified by <i>dwWakeMask</i> and <i>dwFlags</i> have been met. If the conditions have not been met, the calling thread enters the wait state until the conditions of the wait criteria have been met or the time-out interval elapses.

When <i>dwFlags</i> is zero, this function checks the handles in the array in order starting with index 0, until one of the objects is signaled. If multiple objects become signaled, the function returns the index of the first handle in the array whose object was signaled.

<b>MsgWaitForMultipleObjectsEx</b> does not return if there is unread input of the specified type in the message queue after the thread has called a function to check the queue, unless you use the <b>MWMO_INPUTAVAILABLE</b> flag. This is because functions such as 
<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, 
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a>, 
<a href="/windows/desktop/direct3d10/id3dx10threadpump-getqueuestatus">GetQueueStatus</a>, and 
<a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a> check the queue and then change the state information for the queue so that the input is no longer considered new. A subsequent call to 
<b>MsgWaitForMultipleObjectsEx</b> will not return until new input of the specified type arrives, unless you use the <b>MWMO_INPUTAVAILABLE</b> flag. If this flag is not used, the existing unread input (received prior to the last time the thread checked the queue) is ignored.

The function modifies the state of some types of synchronization objects. Modification occurs only for the object or objects whose signaled state caused the function to return. For example, the system decreases the count of a semaphore object by one. For more information, see the documentation for the individual synchronization objects.

The 
<b>MsgWaitForMultipleObjectsEx</b> function can specify handles of any of the following object types in the <i>pHandles</i> array:

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

## -see-also

<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>
