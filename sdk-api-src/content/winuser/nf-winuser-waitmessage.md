---
UID: NF:winuser.WaitMessage
title: WaitMessage function (winuser.h)
description: Yields control to other threads when a thread has no other messages in its message queue. The WaitMessage function suspends the thread and does not return until a new message is placed in the thread's message queue.
helpviewer_keywords: ["WaitMessage","WaitMessage function [Windows and Messages]","_win32_WaitMessage","_win32_waitmessage_cpp","winmsg.waitmessage","winui._win32_waitmessage","winuser/WaitMessage"]
old-location: winmsg\waitmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\waitmessage.htm
ms.date: 12/05/2018
ms.keywords: WaitMessage, WaitMessage function [Windows and Messages], _win32_WaitMessage, _win32_waitmessage_cpp, winmsg.waitmessage, winui._win32_waitmessage, winuser/WaitMessage
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - WaitMessage
 - winuser/WaitMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-message-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - WaitMessage
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# WaitMessage function


## -description

Yields control to other threads when a thread has no other messages in its message queue. The <b>WaitMessage</b> function suspends the thread and does not return until a new message is placed in the thread's message queue.



## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Note that <b>WaitMessage</b> does not return if there is unread input in the message queue after the thread has called a function to check the queue. This is because functions such as <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getqueuestatus">GetQueueStatus</a>, <b>WaitMessage</b>, <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> check the queue and then change the state information for the queue so that the input is no longer considered new. A subsequent call to <b>WaitMessage</b> will not return until new input of the specified type arrives. The existing unread input (received prior to the last time the thread checked the queue) is ignored.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>
