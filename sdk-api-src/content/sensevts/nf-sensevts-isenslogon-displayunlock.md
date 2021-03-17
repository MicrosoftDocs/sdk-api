---
UID: NF:sensevts.ISensLogon.DisplayUnlock
title: ISensLogon::DisplayUnlock (sensevts.h)
description: The DisplayUnLock method notifies an application that the screen display is unlocked.
helpviewer_keywords: ["DisplayUnLock method [SENS]","DisplayUnLock method [SENS]","ISensLogon interface","DisplayUnlock","ISensLogon interface [SENS]","DisplayUnLock method","ISensLogon.DisplayUnlock","ISensLogon::DisplayUnLock","ISensLogon::DisplayUnlock","_zaw_isenslogon_displayunlock","sens.isenslogon_displayunlock","sensevts/ISensLogon::DisplayUnLock","syncmgr.isenslogon_displayunlock"]
old-location: sens\isenslogon_displayunlock.htm
tech.root: Sens
ms.assetid: aa1b1beb-f59a-4990-84e1-deca1432f6cf
ms.date: 12/05/2018
ms.keywords: DisplayUnLock method [SENS], DisplayUnLock method [SENS],ISensLogon interface, DisplayUnlock, ISensLogon interface [SENS],DisplayUnLock method, ISensLogon.DisplayUnlock, ISensLogon::DisplayUnLock, ISensLogon::DisplayUnlock, _zaw_isenslogon_displayunlock, sens.isenslogon_displayunlock, sensevts/ISensLogon::DisplayUnLock, syncmgr.isenslogon_displayunlock
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
 - ISensLogon::DisplayUnlock
 - sensevts/ISensLogon::DisplayUnlock
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
 - ISensLogon.DisplayUnLock
---

# ISensLogon::DisplayUnlock


## -description

The 
<b>DisplayUnLock</b> method notifies an application that the screen display is unlocked.

## -parameters

### -param bstrUserName [in]

The name of a current user.

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

SENS calls this method to notify an application that the screen display is unlocked.

<div class="alert"><b>Important</b>  This function will not work with multiple logins through Remote Desktop Services and does not support Remote Desktop Services or Fast-User Switching scenarios. Desktop applications can register for session changes notifications by calling <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a>. Services can handle session change notifications via SERVICE_CONTROL_SESSIONCHANGE control codes in their <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> callback function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displaylock">ISensLogon::DisplayLock</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-startscreensaver">ISensLogon::StartScreenSaver</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-stopscreensaver">ISensLogon::StopScreenSaver</a>