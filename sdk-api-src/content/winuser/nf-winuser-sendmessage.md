---
UID: NF:winuser.SendMessage
title: SendMessage function
author: windows-sdk-content
description: Sends the specified message to a window or windows. The SendMessage function calls the window procedure for the specified window and does not return until the window procedure has processed the message.
old-location: winmsg\sendmessage.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessage.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: SendMessage, SendMessage function [Windows and Messages], SendMessageA, SendMessageW, _win32_SendMessage, _win32_sendmessage_cpp, winmsg.sendmessage, winui._win32_sendmessage, winuser/SendMessage, winuser/SendMessageA, winuser/SendMessageW
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
req.unicode-ansi: SendMessageW (Unicode) and SendMessageA (ANSI)
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
 - Ext-MS-Win-NTUser-message-l1-1-0.dll
 - Ext-MS-Win-NTUser-message-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - Ext-MS-Win-NTUser-Message-l1-1-2.dll
 - Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
 - SendMessage
 - SendMessageA
 - SendMessageW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SendMessage function


## -description


Sends the specified message to a window or windows. The <b>SendMessage</b> function calls the window procedure for the specified window and does not return until the window procedure has processed the message.

To send a message and return immediately, use the <a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a> or <a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a> function. To post a message to a thread's message queue and return immediately, use the <a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a> or <a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a> function.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message. If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.

 Message sending is subject to UIPI. The thread of a process can send messages only to message queues of threads in processes of lesser or equal integrity level.


### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="about_messages_and_message_queues.htm">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <strong>Type: <b>LRESULT</b>
</strong>

The return value specifies the result of the message processing; it depends on the message sent.




## -remarks



 When a message is blocked by UIPI the last error, retrieved with <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, is set to 5 (access denied).

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://msdn.microsoft.com/4115c587-fcb4-4170-9948-fe33bcb8742a">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.

If the specified window was created by the calling thread, the window procedure is called immediately as a subroutine. If the specified window was created by a different thread, the system switches to that thread and calls the appropriate window procedure. Messages sent between threads are processed only when the receiving thread executes message retrieval code. The sending thread is blocked until the receiving thread processes the message. However, the sending thread will process incoming nonqueued messages while waiting for its message to be processed. To prevent this, use <a href="https://msdn.microsoft.com/c8096383-9fdf-42b3-af98-0bfe0d02c656">SendMessageTimeout</a> with SMTO_BLOCK set. For more information on nonqueued messages, see <a href="about_messages_and_message_queues.htm">Nonqueued Messages</a>.

 An accessibility application can use <b>SendMessage</b> to send <a href="https://msdn.microsoft.com/ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c">WM_APPCOMMAND</a> messages  to the shell to launch applications. This  functionality is not guaranteed to work for other types of applications.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d08e7f12-6595-4234-bfc4-08daad93e4c4">Displaying Keyboard Input</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/adca4de0-fba5-4a1e-952f-d65bdcca5b0c">InSendMessage</a>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>



<a href="https://msdn.microsoft.com/c418cb0e-1b9f-4ca8-8b02-e6901f7744a6">PostThreadMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/28546e65-0111-4e19-8044-738a76428965">SendDlgItemMessage</a>



<a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/c8096383-9fdf-42b3-af98-0bfe0d02c656">SendMessageTimeout</a>



<a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>
 

 

