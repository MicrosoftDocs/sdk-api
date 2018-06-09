---
UID: NF:wtsapi32.WTSRegisterSessionNotification
title: WTSRegisterSessionNotification function
author: windows-sdk-content
description: Registers the specified window to receive session change notifications.
old-location: termserv\wtsregistersessionnotification.htm
old-project: TermServ
ms.assetid: 5067bb03-d8d5-41ce-b187-04d7dd22a028
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: NOTIFY_FOR_ALL_SESSIONS, NOTIFY_FOR_THIS_SESSION, WTSRegisterSessionNotification, WTSRegisterSessionNotification function [Remote Desktop Services], _win32_wtsregistersessionnotification, termserv.wtsregistersessionnotification, wtsapi32/WTSRegisterSessionNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSRegisterSessionNotification
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSRegisterSessionNotification function


## -description


Registers the specified window to receive session change notifications.


## -parameters




### -param hWnd [in]

Handle of the window to receive session change notifications.


### -param dwFlags [in]

Specifies which session notifications are to be received. This parameter can be one of the following 
      values.



#### NOTIFY_FOR_THIS_SESSION

Only session notifications involving the session attached to by the window identified by the 
        <i>hWnd</i> parameter value are to be received.



#### NOTIFY_FOR_ALL_SESSIONS

All session notifications are to be received.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. Otherwise, it is 
       <b>FALSE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called before the dependent services of Remote Desktop Services have started, an 
    <b>RPC_S_INVALID_BINDING</b> error code may be returned. When the Global\\TermSrvReadyEvent 
    global event is set, all dependent services  have started and this function can be successfully called.

Session change notifications are sent in the form of a 
    <a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a> message. These 
    notifications are sent only to the windows that have registered for them using this function.

When a window no longer requires these notifications, it must call 
    <a href="https://msdn.microsoft.com/654e585a-f0b2-45a1-a58d-fe3505b34b61">WTSUnRegisterSessionNotification</a> 
    before being destroyed. For every call to this function, there must be a corresponding call to 
    <b>WTSUnRegisterSessionNotification</b>.

If the window handle passed in this function is already registered, the value of the <i>dwFlags</i> parameter is ignored.

To receive session change notifications from a service, use the 
    <a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a>



<a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a>



<a href="https://msdn.microsoft.com/9aa43cfa-9518-428b-95a1-004fa23df90b">WTSGetActiveConsoleSessionId</a>



<a href="https://msdn.microsoft.com/8670643e-33e0-482a-ade0-d136b8c97d37">WTSRegisterSessionNotificationEx</a>



<a href="https://msdn.microsoft.com/863bd689-796b-4875-81bf-f853354b08b5">WTSSESSION_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/654e585a-f0b2-45a1-a58d-fe3505b34b61">WTSUnRegisterSessionNotification</a>
 

 

