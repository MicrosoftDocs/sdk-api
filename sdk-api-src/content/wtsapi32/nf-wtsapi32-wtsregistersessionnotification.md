---
UID: NF:wtsapi32.WTSRegisterSessionNotification
title: WTSRegisterSessionNotification function (wtsapi32.h)
description: Registers the specified window to receive session change notifications. (WTSRegisterSessionNotification)
helpviewer_keywords: ["NOTIFY_FOR_ALL_SESSIONS","NOTIFY_FOR_THIS_SESSION","WTSRegisterSessionNotification","WTSRegisterSessionNotification function [Remote Desktop Services]","_win32_wtsregistersessionnotification","termserv.wtsregistersessionnotification","wtsapi32/WTSRegisterSessionNotification"]
old-location: termserv\wtsregistersessionnotification.htm
tech.root: TermServ
ms.assetid: 5067bb03-d8d5-41ce-b187-04d7dd22a028
ms.date: 12/05/2018
ms.keywords: NOTIFY_FOR_ALL_SESSIONS, NOTIFY_FOR_THIS_SESSION, WTSRegisterSessionNotification, WTSRegisterSessionNotification function [Remote Desktop Services], _win32_wtsregistersessionnotification, termserv.wtsregistersessionnotification, wtsapi32/WTSRegisterSessionNotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSRegisterSessionNotification
 - wtsapi32/WTSRegisterSessionNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSRegisterSessionNotification
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
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
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If this function is called before the dependent services of Remote Desktop Services have started, an 
    <b>RPC_S_INVALID_BINDING</b> error code may be returned. When the Global\\TermSrvReadyEvent 
    global event is set, all dependent services  have started and this function can be successfully called.

Session change notifications are sent in the form of a 
    <a href="/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a> message. These 
    notifications are sent only to the windows that have registered for them using this function.

When a window no longer requires these notifications, it must call 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification">WTSUnRegisterSessionNotification</a> 
    before being destroyed. For every call to this function, there must be a corresponding call to 
    <b>WTSUnRegisterSessionNotification</b>.

If the window handle passed in this function is already registered, the value of the <i>dwFlags</i> parameter is ignored.

To receive session change notifications from a service, use the 
    <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> function.

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a>



<a href="/windows/desktop/api/winbase/nf-winbase-wtsgetactiveconsolesessionid">WTSGetActiveConsoleSessionId</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex">WTSRegisterSessionNotificationEx</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wtssession_notification">WTSSESSION_NOTIFICATION</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification">WTSUnRegisterSessionNotification</a>
