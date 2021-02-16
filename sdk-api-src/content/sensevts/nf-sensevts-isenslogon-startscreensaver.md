---
UID: NF:sensevts.ISensLogon.StartScreenSaver
title: ISensLogon::StartScreenSaver (sensevts.h)
description: The StartScreenSaver method notifies an application that a screen saver is started.
helpviewer_keywords: ["ISensLogon interface [SENS]","StartScreenSaver method","ISensLogon.StartScreenSaver","ISensLogon::StartScreenSaver","StartScreenSaver","StartScreenSaver method [SENS]","StartScreenSaver method [SENS]","ISensLogon interface","_zaw_isenslogon_startscreensaver","sens.isenslogon_startscreensaver","sensevts/ISensLogon::StartScreenSaver","syncmgr.isenslogon_startscreensaver"]
old-location: sens\isenslogon_startscreensaver.htm
tech.root: Sens
ms.assetid: 47531e1f-e2d4-4475-a109-e213c903a7ba
ms.date: 12/05/2018
ms.keywords: ISensLogon interface [SENS],StartScreenSaver method, ISensLogon.StartScreenSaver, ISensLogon::StartScreenSaver, StartScreenSaver, StartScreenSaver method [SENS], StartScreenSaver method [SENS],ISensLogon interface, _zaw_isenslogon_startscreensaver, sens.isenslogon_startscreensaver, sensevts/ISensLogon::StartScreenSaver, syncmgr.isenslogon_startscreensaver
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
 - ISensLogon::StartScreenSaver
 - sensevts/ISensLogon::StartScreenSaver
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
 - ISensLogon.StartScreenSaver
---

# ISensLogon::StartScreenSaver


## -description

The 
<b>StartScreenSaver</b> method notifies an application that a screen saver is started.

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

SENS calls this method to notify an application that a screen saver is started.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displaylock">ISensLogon::DisplayLock</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displayunlock">ISensLogon::DisplayUnLock</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-stopscreensaver">ISensLogon::StopScreenSaver</a>