---
UID: NF:wtsapi32.WTSUnRegisterSessionNotificationEx
title: WTSUnRegisterSessionNotificationEx function
author: windows-sdk-content
description: Unregisters the specified window so that it receives no further session change notifications.
old-location: termserv\wtsunregistersessionnotificationex.htm
old-project: TermServ
ms.assetid: 774df4a2-5d66-42fd-94b5-a51d5ba99c94
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: WTSUnRegisterSessionNotificationEx, WTSUnRegisterSessionNotificationEx function [Remote Desktop Services], termserv.wtsunregistersessionnotificationex, wtsapi32/WTSUnRegisterSessionNotificationEx
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
api_name:
 - WTSUnRegisterSessionNotificationEx
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSUnRegisterSessionNotificationEx function


## -description


Unregisters the specified window so that it receives no further session change notifications.


## -parameters




### -param hServer [in]

Handle of the server returned from 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> or 
      <b>WTS_CURRENT_SERVER</b>.


### -param hWnd [in]

Handle of the window to be unregistered from receiving session notifications.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>. To get extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function must be called once for every call to the 
    <a href="https://msdn.microsoft.com/8670643e-33e0-482a-ade0-d136b8c97d37">WTSRegisterSessionNotificationEx</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>



<a href="https://msdn.microsoft.com/8670643e-33e0-482a-ade0-d136b8c97d37">WTSRegisterSessionNotificationEx</a>



<a href="https://msdn.microsoft.com/654e585a-f0b2-45a1-a58d-fe3505b34b61">WTSUnRegisterSessionNotification</a>
 

 

