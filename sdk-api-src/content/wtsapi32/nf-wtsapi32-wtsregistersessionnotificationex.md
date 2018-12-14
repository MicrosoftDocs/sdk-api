---
UID: NF:wtsapi32.WTSRegisterSessionNotificationEx
title: WTSRegisterSessionNotificationEx function
author: windows-sdk-content
description: Registers the specified window to receive session change notifications.
old-location: termserv\wtsregistersessionnotificationex.htm
tech.root: TermServ
ms.assetid: 8670643e-33e0-482a-ade0-d136b8c97d37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NOTIFY_FOR_ALL_SESSIONS, NOTIFY_FOR_THIS_SESSION, WTSRegisterSessionNotificationEx, WTSRegisterSessionNotificationEx function [Remote Desktop Services], termserv.wtsregistersessionnotificationex, wtsapi32/WTSRegisterSessionNotificationEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSRegisterSessionNotificationEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSRegisterSessionNotificationEx function


## -description


Registers the specified window to receive session change notifications.


## -parameters




### -param hServer [in]

Handle of the server returned from 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> or 
      <b>WTS_CURRENT_SERVER</b>.


### -param hWnd [in]

Handle of the window to receive session change notifications.


### -param dwFlags [in]

Specifies which session notifications are to be received. This parameter can only be 
      <b>NOTIFY_FOR_THIS_SESSION</b> if <i>hServer</i> is a remote server.



#### NOTIFY_FOR_THIS_SESSION (0)

Only session notifications involving the session attached to by the window identified by the 
        <i>hWnd</i> parameter value are to be received.



#### NOTIFY_FOR_ALL_SESSIONS (1)

All session notifications are to be received.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. Otherwise, it is 
       <b>FALSE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If this function is called before the dependent services of Remote Desktop Services have started, an 
    <b>RPC_S_INVALID_BINDING</b> error code may be returned. When the 
    "Global\\TermSrvReadyEvent" global event is set, all dependent services  have started and this 
    function can be successfully called.

Session change notifications are sent in the form of a 
    <a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a> message. These 
    notifications are sent only to the windows that have registered for them using this function.

When a window no longer requires these notifications, it must call 
    <a href="https://msdn.microsoft.com/774df4a2-5d66-42fd-94b5-a51d5ba99c94">WTSUnRegisterSessionNotificationEx</a> 
    before being destroyed. For every call to this function, there must be a corresponding call to 
    <b>WTSUnRegisterSessionNotificationEx</b>.

If the window handle passed in this function is already registered, the value of the 
    <i>dwFlags</i> parameter is ignored.

To receive session change notifications from a service, use the 
    <a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a>



<a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a>



<a href="https://msdn.microsoft.com/9aa43cfa-9518-428b-95a1-004fa23df90b">WTSGetActiveConsoleSessionId</a>



<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>



<a href="https://msdn.microsoft.com/863bd689-796b-4875-81bf-f853354b08b5">WTSSESSION_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/774df4a2-5d66-42fd-94b5-a51d5ba99c94">WTSUnRegisterSessionNotificationEx</a>
 

 

