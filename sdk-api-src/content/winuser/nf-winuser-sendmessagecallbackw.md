---
UID: NF:winuser.SendMessageCallbackW
title: SendMessageCallbackW function
author: windows-sdk-content
description: Sends the specified message to a window or windows.
old-location: winmsg\sendmessagecallback.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessagecallback.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SendMessageCallback, SendMessageCallback function [Windows and Messages], SendMessageCallbackA, SendMessageCallbackW, _win32_SendMessageCallback, _win32_sendmessagecallback_cpp, winmsg.sendmessagecallback, winui._win32_sendmessagecallback, winuser/SendMessageCallback, winuser/SendMessageCallbackA, winuser/SendMessageCallbackW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - SendMessageCallback
 - SendMessageCallbackA
 - SendMessageCallbackW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

For lists of the system-provided messages, see <a href="https://msdn.microsoft.com/en-us/library/ms644927(v=VS.85).aspx">System-Defined Messages</a>.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


### -param lpResultCallBack [in]

Type: <b>SENDASYNCPROC</b>

A pointer to a callback function that the system calls after the window procedure processes the message. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms644949(v=VS.85).aspx">SendAsyncProc</a>. 

                    

If <i>hWnd</i> is <b>HWND_BROADCAST</b> ((HWND)0xffff), the system calls the <a href="https://msdn.microsoft.com/en-us/library/ms644949(v=VS.85).aspx">SendAsyncProc</a> callback function once for each top-level window.


### -param dwData [in]

Type: <b>ULONG_PTR</b>

An application-defined value to be sent to the callback function pointed to by the <i>lpCallBack</i> parameter.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the target window belongs to the same thread as the caller, then the window procedure is called synchronously, and the callback function is called immediately after the window procedure returns. If the target window belongs to a different thread from the caller, then the callback function is called only when the thread that called <b>SendMessageCallback</b> also calls <a href="https://msdn.microsoft.com/en-us/library/ms644936(v=VS.85).aspx">GetMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644943(v=VS.85).aspx">PeekMessage</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms644956(v=VS.85).aspx">WaitMessage</a>.

If you send a message in the range below <a href="https://msdn.microsoft.com/en-us/library/ms644931(v=VS.85).aspx">WM_USER</a> to the asynchronous message functions (<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a>, and <b>SendMessageCallback</b>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used. 

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://msdn.microsoft.com/en-us/library/ms644947(v=VS.85).aspx">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://msdn.microsoft.com/en-us/library/ms644931(v=VS.85).aspx">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632590(v=VS.85).aspx">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644944(v=VS.85).aspx">PostMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644947(v=VS.85).aspx">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644949(v=VS.85).aspx">SendAsyncProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644951(v=VS.85).aspx">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644953(v=VS.85).aspx">SendNotifyMessage</a>
 

 

