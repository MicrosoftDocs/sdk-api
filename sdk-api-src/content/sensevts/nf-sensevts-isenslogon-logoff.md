---
UID: NF:sensevts.ISensLogon.Logoff
title: ISensLogon::Logoff (sensevts.h)
description: The Logoff method notifies an application that a user is logged off. (ISensLogon.Logoff)
helpviewer_keywords: ["ISensLogon interface [SENS]","Logoff method","ISensLogon.Logoff","ISensLogon::Logoff","Logoff","Logoff method [SENS]","Logoff method [SENS]","ISensLogon interface","_zaw_isenslogon_logoff","sens.isenslogon_logoff","sensevts/ISensLogon::Logoff","syncmgr.isenslogon_logoff"]
old-location: sens\isenslogon_logoff.htm
tech.root: Sens
ms.assetid: b45658a1-d427-42b2-912c-5e5c36dab280
ms.date: 12/05/2018
ms.keywords: ISensLogon interface [SENS],Logoff method, ISensLogon.Logoff, ISensLogon::Logoff, Logoff, Logoff method [SENS], Logoff method [SENS],ISensLogon interface, _zaw_isenslogon_logoff, sens.isenslogon_logoff, sensevts/ISensLogon::Logoff, syncmgr.isenslogon_logoff
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
 - ISensLogon::Logoff
 - sensevts/ISensLogon::Logoff
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
 - ISensLogon.Logoff
---

# ISensLogon::Logoff


## -description

The 
<b>Logoff</b> method notifies an application that a user is logged off.

## -parameters

### -param bstrUserName [in]

The name of a user who logs off.

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

<div class="alert"><b>Important</b>  This function will not work with multiple logins through Remote Desktop Services and does not support Remote Desktop Services or Fast-User Switching scenarios. Desktop applications can register for session changes notifications by calling <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a>. Services can handle session change notifications via SERVICE_CONTROL_SESSIONCHANGE control codes in their <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> callback function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-logon">ISensLogon::Logon</a>
