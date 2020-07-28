---
UID: NF:sensevts.ISensLogon2.Logon
title: ISensLogon2::Logon (sensevts.h)
description: The Logon method notifies an application that a user is logged on.
helpviewer_keywords: ["ISensLogon2 interface [SENS]","Logon method","ISensLogon2.Logon","ISensLogon2::Logon","Logon","Logon method [SENS]","Logon method [SENS]","ISensLogon2 interface","_zaw_isenslogon2_logon","sens.isenslogon2_logon","sensevts/ISensLogon2::Logon","syncmgr.isenslogon2_logon"]
old-location: sens\isenslogon2_logon.htm
tech.root: Sens
ms.assetid: 36caaccf-0cb3-47b8-b0bc-68f9bb21f235
ms.date: 12/05/2018
ms.keywords: ISensLogon2 interface [SENS],Logon method, ISensLogon2.Logon, ISensLogon2::Logon, Logon, Logon method [SENS], Logon method [SENS],ISensLogon2 interface, _zaw_isenslogon2_logon, sens.isenslogon2_logon, sensevts/ISensLogon2::Logon, syncmgr.isenslogon2_logon
f1_keywords:
- sensevts/ISensLogon2.Logon
dev_langs:
- c++
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
- ISensLogon2.Logon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensLogon2::Logon


## -description


The 
<b>Logon</b> method notifies an application that a user is logged on.


## -parameters




### -param bstrUserName [in]

The name of a user who is logged on.


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



SENS calls this method to notify an application that a user is logged on.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nn-sensevts-isenslogon2">ISensLogon2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logon">ISensLogon::Logon</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/terminal-services-portal">Terminal Services</a>
 

 

