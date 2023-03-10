---
UID: NF:wtsapi32.WTSUnRegisterSessionNotificationEx
title: WTSUnRegisterSessionNotificationEx function (wtsapi32.h)
description: Unregisters the specified window so that it receives no further session change notifications. (WTSUnRegisterSessionNotificationEx)
helpviewer_keywords: ["WTSUnRegisterSessionNotificationEx","WTSUnRegisterSessionNotificationEx function [Remote Desktop Services]","termserv.wtsunregistersessionnotificationex","wtsapi32/WTSUnRegisterSessionNotificationEx"]
old-location: termserv\wtsunregistersessionnotificationex.htm
tech.root: TermServ
ms.assetid: 774df4a2-5d66-42fd-94b5-a51d5ba99c94
ms.date: 12/05/2018
ms.keywords: WTSUnRegisterSessionNotificationEx, WTSUnRegisterSessionNotificationEx function [Remote Desktop Services], termserv.wtsunregistersessionnotificationex, wtsapi32/WTSUnRegisterSessionNotificationEx
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
 - WTSUnRegisterSessionNotificationEx
 - wtsapi32/WTSUnRegisterSessionNotificationEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSUnRegisterSessionNotificationEx
---

# WTSUnRegisterSessionNotificationEx function


## -description

Unregisters the specified window so that it receives no further session change notifications.

## -parameters

### -param hServer [in]

Handle of the server returned from 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or 
      <b>WTS_CURRENT_SERVER</b>.

### -param hWnd [in]

Handle of the window to be unregistered from receiving session notifications.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function must be called once for every call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex">WTSRegisterSessionNotificationEx</a> 
    function.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex">WTSRegisterSessionNotificationEx</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification">WTSUnRegisterSessionNotification</a>
