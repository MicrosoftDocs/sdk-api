---
UID: NF:winuser.SendNotifyMessageW
title: SendNotifyMessageW function (winuser.h)
description: Sends the specified message to a window or windows. (SendNotifyMessageW)
helpviewer_keywords: ["SendNotifyMessage", "SendNotifyMessage function [Windows and Messages]", "SendNotifyMessageW", "_win32_SendNotifyMessage", "_win32_sendnotifymessage_cpp", "winmsg.sendnotifymessage", "winui._win32_sendnotifymessage", "winuser/SendNotifyMessage", "winuser/SendNotifyMessageW"]
old-location: winmsg\sendnotifymessage.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendnotifymessage.htm
ms.date: 12/05/2018
ms.keywords: SendNotifyMessage, SendNotifyMessage function [Windows and Messages], SendNotifyMessageA, SendNotifyMessageW, _win32_SendNotifyMessage, _win32_sendnotifymessage_cpp, winmsg.sendnotifymessage, winui._win32_sendnotifymessage, winuser/SendNotifyMessage, winuser/SendNotifyMessageA, winuser/SendNotifyMessageW
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendNotifyMessageW
 - winuser/SendNotifyMessageW
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
req.apiset: ext-ms-win-ntuser-message-l1-1-3 (introduced in Windows 10, version 10.0.14393)
---

# SendNotifyMessageW function


## -description

Sends the specified message to a window or windows. If the window was created by the calling thread, <b>SendNotifyMessage</b> calls the window procedure for the window and does not return until the window procedure has processed the message. If the window was created by a different thread, <b>SendNotifyMessage</b> passes the message to the window procedure and returns immediately; it does not wait for the window procedure to finish processing the message.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message. If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.

### -param Msg [in]

Type: <b>UINT</b>

The message to be sent.

For lists of the system-provided messages, see <a href="/windows/desktop/winmsg/about-messages-and-message-queues">System-Defined Messages</a>.

### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.

### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If you send a message in the range below <a href="/windows/desktop/winmsg/wm-user">WM_USER</a> to the asynchronous message functions (<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>, <b>SendNotifyMessage</b>, and <a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used.

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.





> [!NOTE]
> The winuser.h header defines SendNotifyMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea">PostThreadMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
