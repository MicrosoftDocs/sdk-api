---
UID: NF:wtsapi32.WTSUnRegisterSessionNotification
title: WTSUnRegisterSessionNotification function (wtsapi32.h)
description: Unregisters the specified window so that it receives no further session change notifications. (WTSUnRegisterSessionNotification)
helpviewer_keywords: ["WTSUnRegisterSessionNotification","WTSUnRegisterSessionNotification function [Remote Desktop Services]","_win32_wtsunregistersessionnotification","termserv.wtsunregistersessionnotification","wtsapi32/WTSUnRegisterSessionNotification"]
old-location: termserv\wtsunregistersessionnotification.htm
tech.root: TermServ
ms.assetid: 654e585a-f0b2-45a1-a58d-fe3505b34b61
ms.date: 12/05/2018
ms.keywords: WTSUnRegisterSessionNotification, WTSUnRegisterSessionNotification function [Remote Desktop Services], _win32_wtsunregistersessionnotification, termserv.wtsunregistersessionnotification, wtsapi32/WTSUnRegisterSessionNotification
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
 - WTSUnRegisterSessionNotification
 - wtsapi32/WTSUnRegisterSessionNotification
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
 - WTSUnRegisterSessionNotification
req.apiset: ext-ms-win-session-wtsapi32-l1-1-0 (introduced in Windows 8)
---

# WTSUnRegisterSessionNotification function


## -description

Unregisters the specified window 
    so that it receives no further session change notifications.

## -parameters

### -param hWnd [in]

Handle of the window to be unregistered from receiving session notifications.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function must be called once for every call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a> 
    function.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex">WTSUnRegisterSessionNotificationEx</a>
