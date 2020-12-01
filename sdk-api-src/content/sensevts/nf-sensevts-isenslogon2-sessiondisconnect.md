---
UID: NF:sensevts.ISensLogon2.SessionDisconnect
title: ISensLogon2::SessionDisconnect (sensevts.h)
description: The SessionDisconnect method is used to disconnect from a Fast User Switching session or a Remote Desktop Connection. This is different from logging off from a session, because when you use this method the session is disconnected.
helpviewer_keywords: ["ISensLogon2 interface [SENS]","SessionDisconnect method","ISensLogon2.SessionDisconnect","ISensLogon2::SessionDisconnect","SessionDisconnect","SessionDisconnect method [SENS]","SessionDisconnect method [SENS]","ISensLogon2 interface","_zaw_isenslogon2_sessiondisconnect","sens.isenslogon2_sessiondisconnect","sensevts/ISensLogon2::SessionDisconnect","syncmgr.isenslogon2_sessiondisconnect"]
old-location: sens\isenslogon2_sessiondisconnect.htm
tech.root: Sens
ms.assetid: afa56cb1-7c52-48db-ac7c-237cb49cc97f
ms.date: 12/05/2018
ms.keywords: ISensLogon2 interface [SENS],SessionDisconnect method, ISensLogon2.SessionDisconnect, ISensLogon2::SessionDisconnect, SessionDisconnect, SessionDisconnect method [SENS], SessionDisconnect method [SENS],ISensLogon2 interface, _zaw_isenslogon2_sessiondisconnect, sens.isenslogon2_sessiondisconnect, sensevts/ISensLogon2::SessionDisconnect, syncmgr.isenslogon2_sessiondisconnect
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
 - ISensLogon2::SessionDisconnect
 - sensevts/ISensLogon2::SessionDisconnect
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
 - ISensLogon2.SessionDisconnect
---

# ISensLogon2::SessionDisconnect


## -description

The 
<b>SessionDisconnect</b> method is used to disconnect from a Fast User Switching session or a Remote Desktop Connection. This is different from logging off from a session, because when you use this method the session is disconnected.

## -parameters

### -param bstrUserName [in]

The name of a current user.

### -param dwSessionId [in]

The session identifier of a session.

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
The method returns successfully.

</td>
</tr>
</table>

## -remarks

SENS calls this method to notify an application that a session is disconnected.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon2">ISensLogon2</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logoff">ISensLogon::Logoff</a>



<a href="/windows/desktop/TermServ/terminal-services-portal">Terminal Services</a>