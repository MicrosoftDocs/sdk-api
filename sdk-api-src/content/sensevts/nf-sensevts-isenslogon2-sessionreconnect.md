---
UID: NF:sensevts.ISensLogon2.SessionReconnect
title: ISensLogon2::SessionReconnect
author: windows-sdk-content
description: The session was reconnected. The SessionReconnect method is used when you reconnect to a Fast User Switching session or a Remote Desktop Connection. This is different from logging on to a new session.
old-location: sens\isenslogon2_sessionreconnect.htm
tech.root: Sens
ms.assetid: b789a75d-e842-40b4-9e8d-b9374b5ba6b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISensLogon2 interface [SENS],SessionReconnect method, ISensLogon2.SessionReconnect, ISensLogon2::SessionReconnect, SessionReconnect, SessionReconnect method [SENS], SessionReconnect method [SENS],ISensLogon2 interface, _zaw_isenslogon2_sessionreconnect, sens.isenslogon2_sessionreconnect, sensevts/ISensLogon2::SessionReconnect, syncmgr.isenslogon2_sessionreconnect
ms.topic: method
req.header: sensevts.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Sensevts.tlb
req.lib: 
req.dll: Sens.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensLogon2.SessionReconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensLogon2::SessionReconnect


## -description


The session was reconnected. The 
<b>SessionReconnect</b> method is used when you reconnect to a Fast User Switching session or a Remote Desktop Connection. This is different from logging on to a new session.


## -parameters




### -param bstrUserName [in]

Name of the current user.


### -param dwSessionId [in]

The session identifier of the session.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method returned successfully.

</td>
</tr>
</table>
 




## -remarks



SENS calls this method to notify your application that the session was reconnected.




## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/be61b5b9-d4f1-40ea-a734-7b02c06e41e8">ISensLogon2</a>



<a href="https://msdn.microsoft.com/b45658a1-d427-42b2-912c-5e5c36dab280">ISensLogon::Logoff</a>



<a href="https://msdn.microsoft.com/90c40b7a-e324-43fc-a1e6-f29997ed9436">Terminal Services</a>
 

 

