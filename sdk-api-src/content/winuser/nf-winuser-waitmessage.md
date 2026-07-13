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
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-message-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
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

Blocks thread execution until the thread needs to process a new message.
The new message could be an input message, a queued message, or a non-queued message.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Note that <b>WaitMessage</b> does not return for unprocessed messages reported by a previous function which checks the queue. This is because functions such as <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-getqueuestatus">GetQueueStatus</a>, <b>WaitMessage</b>, <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> check the queue and then change the state information for the queue so that the message is no longer considered new. A subsequent call to <b>WaitMessage</b> will not return until new messages arrive. The existing unprocessed messages (received prior to the last time the thread checked the queue) are not considered to be new.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>



<b>Reference</b>
