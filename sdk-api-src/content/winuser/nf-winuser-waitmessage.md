---
UID: NF:winuser.WaitMessage
title: WaitMessage function (winuser.h)
author: windows-sdk-content
description: Yields control to other threads when a thread has no other messages in its message queue. The WaitMessage function suspends the thread and does not return until a new message is placed in the thread's message queue.
old-location: winmsg\waitmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\waitmessage.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WaitMessage, WaitMessage function [Windows and Messages], _win32_WaitMessage, _win32_waitmessage_cpp, winmsg.waitmessage, winui._win32_waitmessage, winuser/WaitMessage
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WaitMessage function


## -description


Yields control to other threads when a thread has no other messages in its message queue. The <b>WaitMessage</b> function suspends the thread and does not return until a new message is placed in the thread's message queue.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Note that <b>WaitMessage</b> does not return if there is unread input in the message queue after the thread has called a function to check the queue. This is because functions such as <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644940(v=VS.85).aspx">GetQueueStatus</a>, <b>WaitMessage</b>, <a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a>, and <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a> check the queue and then change the state information for the queue so that the input is no longer considered new. A subsequent call to <b>WaitMessage</b> will not return until new input of the specified type arrives. The existing unread input (received prior to the last time the thread checked the queue) is ignored. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>



<b>Reference</b>
 

 

