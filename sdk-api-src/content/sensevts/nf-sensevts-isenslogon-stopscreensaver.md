---
UID: NF:sensevts.ISensLogon.StopScreenSaver
title: ISensLogon::StopScreenSaver (sensevts.h)
description: The StopScreenSaver method notifies an application that a screen saver is stopped.
helpviewer_keywords: ["ISensLogon interface [SENS]","StopScreenSaver method","ISensLogon.StopScreenSaver","ISensLogon::StopScreenSaver","StopScreenSaver","StopScreenSaver method [SENS]","StopScreenSaver method [SENS]","ISensLogon interface","_zaw_isenslogon_stopscreensaver","sens.isenslogon_stopscreensaver","sensevts/ISensLogon::StopScreenSaver","syncmgr.isenslogon_stopscreensaver"]
old-location: sens\isenslogon_stopscreensaver.htm
tech.root: Sens
ms.assetid: 61a6434b-1a80-4a37-9175-636c3792a865
ms.date: 12/05/2018
ms.keywords: ISensLogon interface [SENS],StopScreenSaver method, ISensLogon.StopScreenSaver, ISensLogon::StopScreenSaver, StopScreenSaver, StopScreenSaver method [SENS], StopScreenSaver method [SENS],ISensLogon interface, _zaw_isenslogon_stopscreensaver, sens.isenslogon_stopscreensaver, sensevts/ISensLogon::StopScreenSaver, syncmgr.isenslogon_stopscreensaver
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
 - ISensLogon::StopScreenSaver
 - sensevts/ISensLogon::StopScreenSaver
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
 - ISensLogon.StopScreenSaver
---

# ISensLogon::StopScreenSaver


## -description

The 
<b>StopScreenSaver</b> method notifies an application that a screen saver is stopped.

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

SENS calls this method to notify an application that a screen saver is stopped.

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">IEventSubscription::PutPublisherProperty</a>



<a href="/windows/desktop/api/sensevts/nn-sensevts-isenslogon">ISensLogon</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displaylock">ISensLogon::DisplayLock</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-displayunlock">ISensLogon::DisplayUnLock</a>



<a href="/windows/desktop/api/sensevts/nf-sensevts-isenslogon-startscreensaver">ISensLogon::StartScreenSaver</a>