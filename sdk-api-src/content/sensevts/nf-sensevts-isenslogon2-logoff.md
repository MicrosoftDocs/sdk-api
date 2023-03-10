---
UID: NF:sensevts.ISensLogon2.Logoff
title: ISensLogon2::Logoff (sensevts.h)
description: The Logoff method notifies an application that a user is logged off. (ISensLogon2.Logoff)
helpviewer_keywords: ["ISensLogon2 interface [SENS]","Logoff method","ISensLogon2.Logoff","ISensLogon2::Logoff","Logoff","Logoff method [SENS]","Logoff method [SENS]","ISensLogon2 interface","_zaw_isenslogon2_logoff","sens.isenslogon2_logoff","sensevts/ISensLogon2::Logoff","syncmgr.isenslogon2_logoff"]
old-location: sens\isenslogon2_logoff.htm
tech.root: Sens
ms.assetid: a366a9ca-ce3a-4800-90c6-e1ba53e4cb30
ms.date: 12/05/2018
ms.keywords: ISensLogon2 interface [SENS],Logoff method, ISensLogon2.Logoff, ISensLogon2::Logoff, Logoff, Logoff method [SENS], Logoff method [SENS],ISensLogon2 interface, _zaw_isenslogon2_logoff, sens.isenslogon2_logoff, sensevts/ISensLogon2::Logoff, syncmgr.isenslogon2_logoff
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
 - ISensLogon2::Logoff
 - sensevts/ISensLogon2::Logoff
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
 - ISensLogon2.Logoff
---

# ISensLogon2::Logoff


## -description

The 
<b>Logoff</b> method notifies an application that a user is logged off.

## -parameters

### -param bstrUserName [in]

The name of a user who logs off.

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

SENS calls this method to notify an application that a user is logged off.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon2">ISensLogon2</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logoff">ISensLogon::Logoff</a>



<a href="/windows/desktop/TermServ/terminal-services-portal">Terminal Services</a>
