---
UID: NF:sensevts.ISensLogon2.SessionReconnect
title: ISensLogon2::SessionReconnect (sensevts.h)
description: The session was reconnected. The SessionReconnect method is used when you reconnect to a Fast User Switching session or a Remote Desktop Connection. This is different from logging on to a new session.
helpviewer_keywords: ["ISensLogon2 interface [SENS]","SessionReconnect method","ISensLogon2.SessionReconnect","ISensLogon2::SessionReconnect","SessionReconnect","SessionReconnect method [SENS]","SessionReconnect method [SENS]","ISensLogon2 interface","_zaw_isenslogon2_sessionreconnect","sens.isenslogon2_sessionreconnect","sensevts/ISensLogon2::SessionReconnect","syncmgr.isenslogon2_sessionreconnect"]
old-location: sens\isenslogon2_sessionreconnect.htm
tech.root: Sens
ms.assetid: b789a75d-e842-40b4-9e8d-b9374b5ba6b0
ms.date: 12/05/2018
ms.keywords: ISensLogon2 interface [SENS],SessionReconnect method, ISensLogon2.SessionReconnect, ISensLogon2::SessionReconnect, SessionReconnect, SessionReconnect method [SENS], SessionReconnect method [SENS],ISensLogon2 interface, _zaw_isenslogon2_sessionreconnect, sens.isenslogon2_sessionreconnect, sensevts/ISensLogon2::SessionReconnect, syncmgr.isenslogon2_sessionreconnect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensLogon2::SessionReconnect
 - sensevts/ISensLogon2::SessionReconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sens.dll
api_name:
 - ISensLogon2.SessionReconnect
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

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon2">ISensLogon2</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logoff">ISensLogon::Logoff</a>



<a href="/windows/desktop/TermServ/terminal-services-portal">Terminal Services</a>