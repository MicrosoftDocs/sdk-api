---
UID: NF:wtsapi32.WTSRegisterSessionNotificationEx
title: WTSRegisterSessionNotificationEx function (wtsapi32.h)
description: Registers the specified window to receive session change notifications.helpviewer_keywords: ["NOTIFY_FOR_ALL_SESSIONS","NOTIFY_FOR_THIS_SESSION","WTSRegisterSessionNotificationEx","WTSRegisterSessionNotificationEx function [Remote Desktop Services]","termserv.wtsregistersessionnotificationex","wtsapi32/WTSRegisterSessionNotificationEx"]
old-location: termserv\wtsregistersessionnotificationex.htm
tech.root: TermServ
ms.assetid: 8670643e-33e0-482a-ade0-d136b8c97d37
ms.date: 12/05/2018
ms.keywords: NOTIFY_FOR_ALL_SESSIONS, NOTIFY_FOR_THIS_SESSION, WTSRegisterSessionNotificationEx, WTSRegisterSessionNotificationEx function [Remote Desktop Services], termserv.wtsregistersessionnotificationex, wtsapi32/WTSRegisterSessionNotificationEx
f1_keywords:
- wtsapi32/WTSRegisterSessionNotificationEx
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSRegisterSessionNotificationEx function


## -description


Registers the specified window to receive session change notifications.


## -parameters




### -param hServer [in]

Handle of the server returned from 
      <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or 
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
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If this function is called before the dependent services of Remote Desktop Services have started, an 
    <b>RPC_S_INVALID_BINDING</b> error code may be returned. When the 
    "Global\\TermSrvReadyEvent" global event is set, all dependent services  have started and this 
    function can be successfully called.

Session change notifications are sent in the form of a 
    <a href="https://docs.microsoft.com/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a> message. These 
    notifications are sent only to the windows that have registered for them using this function.

When a window no longer requires these notifications, it must call 
    <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex">WTSUnRegisterSessionNotificationEx</a> 
    before being destroyed. For every call to this function, there must be a corresponding call to 
    <b>WTSUnRegisterSessionNotificationEx</b>.

If the window handle passed in this function is already registered, the value of the 
    <i>dwFlags</i> parameter is ignored.

To receive session change notifications from a service, use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-wtsgetactiveconsolesessionid">WTSGetActiveConsoleSessionId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-wtssession_notification">WTSSESSION_NOTIFICATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex">WTSUnRegisterSessionNotificationEx</a>
 

 

