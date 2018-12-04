---
UID: NF:winuser.SendMessageCallbackA
title: SendMessageCallbackA function
author: windows-sdk-content
description: Sends the specified message to a window or windows.
old-location: winmsg\sendmessagecallback.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues\messagesandmessagequeuesreference\messagesandmessagequeuesfunctions\sendmessagecallback.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
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

# SendMessageCallbackA function


## -description


Sends the specified message to a window or windows. It calls the window procedure for the specified window and returns immediately if the window belongs to another thread. After the window procedure processes the message, the system calls the specified callback function, passing the result of the message processing and an application-defined value to the callback function.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose window procedure will receive the message. If this parameter is <b>HWND_BROADCAST</b> ((HWND)0xffff), the message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.


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


### -param lpResultCallBack [in]

Type: <b>SENDASYNCPROC</b>

A pointer to a callback function that the system calls after the window procedure processes the message. For more information, see <a href="https://msdn.microsoft.com/62e1ef8a-b5a8-4969-9e97-d4a601685c27">SendAsyncProc</a>. 

                    

If <i>hWnd</i> is <b>HWND_BROADCAST</b> ((HWND)0xffff), the system calls the <a href="https://msdn.microsoft.com/62e1ef8a-b5a8-4969-9e97-d4a601685c27">SendAsyncProc</a> callback function once for each top-level window.


### -param dwData [in]

Type: <b>ULONG_PTR</b>

An application-defined value to be sent to the callback function pointed to by the <i>lpCallBack</i> parameter.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the target window belongs to the same thread as the caller, then the window procedure is called synchronously, and the callback function is called immediately after the window procedure returns. If the target window belongs to a different thread from the caller, then the callback function is called only when the thread that called <b>SendMessageCallback</b> also calls <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>, <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a>, or <a href="https://msdn.microsoft.com/154fc22f-ef7a-42df-9f5d-26f0d2a2773c">WaitMessage</a>.

If you send a message in the range below <a href="https://msdn.microsoft.com/4115c587-fcb4-4170-9948-fe33bcb8742a">WM_USER</a> to the asynchronous message functions (<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>, <a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>, and <b>SendMessageCallback</b>), its message parameters cannot include pointers. Otherwise, the operation will fail. The functions will return before the receiving thread has had a chance to process the message and the sender will free the memory before it is used. 

Applications that need to communicate using <b>HWND_BROADCAST</b> should use the <a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a> function to obtain a unique message for inter-application communication.

The system only does marshalling for system messages (those in the range 0 to (<a href="https://msdn.microsoft.com/4115c587-fcb4-4170-9948-fe33bcb8742a">WM_USER</a>-1)). To send other messages (those &gt;= <b>WM_USER</b>) to another process, you must do custom marshalling.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/885bb607-3ec0-4e24-9f55-fbdfb1c538a1">Messages and Message Queues</a>



<a href="https://msdn.microsoft.com/5357de37-1e44-4e4a-bdae-b5a386032dd4">PostMessage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/51ddc767-ffce-42bf-885a-24b9ee1b25f0">RegisterWindowMessage</a>



<a href="https://msdn.microsoft.com/62e1ef8a-b5a8-4969-9e97-d4a601685c27">SendAsyncProc</a>



<a href="https://msdn.microsoft.com/6246e7ae-da06-4b86-b0d5-1743522b1bda">SendMessageCallback</a>



<a href="https://msdn.microsoft.com/08767153-34f5-4d31-9705-5a1862b9dd10">SendNotifyMessage</a>
 

 

