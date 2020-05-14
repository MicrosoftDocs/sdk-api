---
UID: NF:winuser.SendMessageW
title: SendMessageW function (winuser.h)
description: Sends the specified message to a window or windows. The SendMessage function calls the window procedure for the specified window and does not return until the window procedure has processed the message.helpviewer_keywords: ["SendMessage","SendMessage function [Windows and Messages]","SendMessageA","SendMessageW","_win32_SendMessage","_win32_sendmessage_cpp","winmsg.sendmessage","winui._win32_sendmessage","winuser/SendMessage","winuser/SendMessageA","winuser/SendMessageW"]
old-location: winmsg\sendmessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessage.htm
ms.date: 12/05/2018
ms.keywords: SendMessage, SendMessage function [Windows and Messages], SendMessageA, SendMessageW, _win32_SendMessage, _win32_sendmessage_cpp, winmsg.sendmessage, winui._win32_sendmessage, winuser/SendMessage, winuser/SendMessageA, winuser/SendMessageW
f1_keywords:
- winuser/SendMessage
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
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
- Ext-MS-Win-NTUser-message-l1-1-0.dll
- Ext-MS-Win-NTUser-message-l1-1-1.dll
- Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
- Ext-MS-Win-NTUser-Message-l1-1-2.dll
- Ext-MS-Win-NTUser-Message-L1-1-3.dll
api_name:
- SendMessage
- SendMessageA
- SendMessageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SendMessageW function


## -description


Sends the specified message to a window or windows. The <b>SendMessage</b> function calls the window procedure for the specified window and does not return until the window procedure has processed the message.

To send a message and return immediately, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a> function. To post a message to a thread's message queue and return immediately, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a> function.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message. If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.

 Message sending is subject to UIPI. The thread of a process can send messages only to message queues of threads in processes of lesser or equal integrity level.


### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>LRESULT</b>

The return value specifies the result of the message processing; it depends on the message sent.




## -remarks



 When a message is blocked by UIPI the last error, retrieved with <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, is set to 5 (access denied).

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.

If the specified window was created by the calling thread, the window procedure is called immediately as a subroutine. If the specified window was created by a different thread, the system switches to that thread and calls the appropriate window procedure. Messages sent between threads are processed only when the receiving thread executes message retrieval code. The sending thread is blocked until the receiving thread processes the message. However, the sending thread will process incoming nonqueued messages while waiting for its message to be processed. To prevent this, use <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessagetimeouta">SendMessageTimeout</a> with SMTO_BLOCK set. For more information on nonqueued messages, see <a href="https://docs.microsoft.com/windows/desktop/winmsg/about-messages-and-message-queues">Nonqueued Messages</a>.

 An accessibility application can use <b>SendMessage</b> to send <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-appcommand">WM_APPCOMMAND</a> messages  to the shell to launch applications. This  functionality is not guaranteed to work for other types of applications.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/inputdev/using-keyboard-input">Displaying Keyboard Input</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-insendmessage">InSendMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea">SendDlgItemMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessagetimeouta">SendMessageTimeout</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
 

 

