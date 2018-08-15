---
UID: NF:winuser.SendNotifyMessageA
title: SendNotifyMessageA function
author: windows-sdk-content
description: Sends the specified message to a window or windows.
old-location: winmsg\sendnotifymessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendnotifymessage.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SendNotifyMessage, SendNotifyMessage function [Windows and Messages], SendNotifyMessageA, SendNotifyMessageW, _win32_SendNotifyMessage, _win32_sendnotifymessage_cpp, winmsg.sendnotifymessage, winui._win32_sendnotifymessage, winuser/SendNotifyMessage, winuser/SendNotifyMessageA, winuser/SendNotifyMessageW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SendNotifyMessageW (Unicode) and SendNotifyMessageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - SendNotifyMessage
 - SendNotifyMessageA
 - SendNotifyMessageW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SendNotifyMessageA function


## -description


Sends the specified message to a window or windows. If the window was created by the calling thread, <b>SendNotifyMessage</b> calls the window procedure for the window and does not return until the window procedure has processed the message. If the window was created by a different thread, <b>SendNotifyMessage</b> passes the message to the window procedure and returns immediately; it does not wait for the window procedure to finish processing the message.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message. If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.


### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="https://msdn.microsoft.com/en-us/library/ms644927(v=VS.85).aspx">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If you send a message in the range below <a href="https://msdn.microsoft.com/en-us/library/ms644931(v=VS.85).aspx">WM_USER</a> to the asynchronous message functions (<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>, <b>SendNotifyMessage</b>, and <a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used.

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://msdn.microsoft.com/en-us/library/ms644947(v=VS.85).aspx">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://msdn.microsoft.com/en-us/library/ms644931(v=VS.85).aspx">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644946(v=VS.85).aspx">PostThreadMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644947(v=VS.85).aspx">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a>
 

 

