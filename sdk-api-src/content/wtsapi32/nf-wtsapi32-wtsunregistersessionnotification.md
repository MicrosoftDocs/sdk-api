---
UID: NF:wtsapi32.WTSUnRegisterSessionNotification
title: WTSUnRegisterSessionNotification function (wtsapi32.h)
author: windows-sdk-content
description: Unregisters the specified window so that it receives no further session change notifications.
old-location: termserv\wtsunregistersessionnotification.htm
tech.root: TermServ
ms.assetid: 654e585a-f0b2-45a1-a58d-fe3505b34b61
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSUnRegisterSessionNotification, WTSUnRegisterSessionNotification function [Remote Desktop Services], _win32_wtsunregistersessionnotification, termserv.wtsunregistersessionnotification, wtsapi32/WTSUnRegisterSessionNotification
ms.topic: function
f1_keywords: 
 - "wtsapi32/WTSUnRegisterSessionNotification"
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
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSUnRegisterSessionNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
       information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function must be called once for every call to the 
    <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a> 
    function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex">WTSUnRegisterSessionNotificationEx</a>
 

 

