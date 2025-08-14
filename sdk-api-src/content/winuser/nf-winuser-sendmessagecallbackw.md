---
UID: NF:winuser.SendMessageCallbackW
title: SendMessageCallbackW function (winuser.h)
description: Sends the specified message to a window or windows. (SendMessageCallbackW)
helpviewer_keywords: ["SendMessageCallback", "SendMessageCallback function [Windows and Messages]", "SendMessageCallbackW", "_win32_SendMessageCallback", "_win32_sendmessagecallback_cpp", "winmsg.sendmessagecallback", "winui._win32_sendmessagecallback", "winuser/SendMessageCallback", "winuser/SendMessageCallbackW"]
old-location: winmsg\sendmessagecallback.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessagecallback.htm
ms.date: 12/05/2018
ms.keywords: SendMessageCallback, SendMessageCallback function [Windows and Messages], SendMessageCallbackA, SendMessageCallbackW, _win32_SendMessageCallback, _win32_sendmessagecallback_cpp, winmsg.sendmessagecallback, winui._win32_sendmessagecallback, winuser/SendMessageCallback, winuser/SendMessageCallbackA, winuser/SendMessageCallbackW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SendMessageCallbackW (Unicode) and SendMessageCallbackA (ANSI)
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
 - SendMessageCallbackW
 - winuser/SendMessageCallbackW
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
 - ext-ms-win-ntuser-message-l1-1-3.dll
 - ext-ms-win-ntuser-message-l1-1-2.dll
 - ext-ms-win-ntuser-message-l1-1-1.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - SendMessageCallback
 - SendMessageCallbackA
 - SendMessageCallbackW
req.apiset: ext-ms-win-ntuser-message-l1-1-0 (introduced in Windows 8)
---

# SendMessageCallbackW function


## -description

Sends the specified message to a window or windows. It calls the window procedure for the specified window and returns immediately if the window belongs to another thread. After the window procedure processes the message, the system calls the specified callback function, passing the result of the message processing and an application-defined value to the callback function.

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

### -param lpResultCallBack [in]

Type: <b>SENDASYNCPROC</b>

A pointer to a callback function that the system calls after the window procedure processes the message. For more information, see <a href="/windows/desktop/api/winuser/nc-winuser-sendasyncproc">SendAsyncProc</a>. 

                    

If <i>hWnd</i> is <b>HWND_BROADCAST</b> ((HWND)0xffff), the system calls the <a href="/windows/desktop/api/winuser/nc-winuser-sendasyncproc">SendAsyncProc</a> callback function once for each top-level window.

### -param dwData [in]

Type: <b>ULONG_PTR</b>

An application-defined value to be sent to the callback function pointed to by the <i>lpCallBack</i> parameter.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the target window belongs to the same thread as the caller, then the window procedure is called synchronously, and the callback function is called immediately after the window procedure returns. If the target window belongs to a different thread from the caller, then the callback function is called only when the thread that called <b>SendMessageCallback</b> also calls <a href="/windows/desktop/api/winuser/nf-winuser-getmessage">GetMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-waitmessage">WaitMessage</a>.

If you send a message in the range below <a href="/windows/desktop/winmsg/wm-user">WM_USER</a> to the asynchronous message functions (<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>, <a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>, and <b>SendMessageCallback</b>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used. 

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="/windows/desktop/winmsg/wm-user">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.





> [!NOTE]
> The winuser.h header defines SendMessageCallback as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/messages-and-message-queues">Messages and Message Queues</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>



<a href="/windows/desktop/api/winuser/nc-winuser-sendasyncproc">SendAsyncProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessagecallbacka">SendMessageCallback</a>



<a href="/windows/desktop/api/winuser/nf-winuser-sendnotifymessagea">SendNotifyMessage</a>
