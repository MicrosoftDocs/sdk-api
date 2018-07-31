---
UID: NF:wtsapi32.WTSUnRegisterSessionNotification
title: WTSUnRegisterSessionNotification function
author: windows-sdk-content
description: Unregisters the specified window so that it receives no further session change notifications.
old-location: termserv\wtsunregistersessionnotification.htm
old-project: TermServ
ms.assetid: 654e585a-f0b2-45a1-a58d-fe3505b34b61
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WTSUnRegisterSessionNotification, WTSUnRegisterSessionNotification function [Remote Desktop Services], _win32_wtsunregistersessionnotification, termserv.wtsunregistersessionnotification, wtsapi32/WTSUnRegisterSessionNotification
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
 - WTSUnRegisterSessionNotification
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function must be called once for every call to the 
    <a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a>



<a href="https://msdn.microsoft.com/774df4a2-5d66-42fd-94b5-a51d5ba99c94">WTSUnRegisterSessionNotificationEx</a>
 

 

