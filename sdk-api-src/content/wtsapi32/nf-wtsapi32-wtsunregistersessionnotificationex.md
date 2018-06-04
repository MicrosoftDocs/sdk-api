---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

