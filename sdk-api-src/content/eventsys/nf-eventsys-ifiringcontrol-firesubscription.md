---
UID: NF:eventsys.IFiringControl.FireSubscription
title: IFiringControl::FireSubscription (eventsys.h)
description: Fires an event to a single subscriber.
helpviewer_keywords: ["FireSubscription","FireSubscription method [COM+]","FireSubscription method [COM+]","IFiringControl interface","IFiringControl interface [COM+]","FireSubscription method","IFiringControl.FireSubscription","IFiringControl::FireSubscription","_cos_IFiringControl_FireSubscriptio","cos.ifiringcontrol_firesubscription","eventsys/IFiringControl::FireSubscription"]
old-location: cos\ifiringcontrol_firesubscription.htm
tech.root: cos
ms.assetid: 64aaa99c-70e0-4a96-ab16-2f5b5666d1c4
ms.date: 12/05/2018
ms.keywords: FireSubscription, FireSubscription method [COM+], FireSubscription method [COM+],IFiringControl interface, IFiringControl interface [COM+],FireSubscription method, IFiringControl.FireSubscription, IFiringControl::FireSubscription, _cos_IFiringControl_FireSubscriptio, cos.ifiringcontrol_firesubscription, eventsys/IFiringControl::FireSubscription
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFiringControl::FireSubscription
 - eventsys/IFiringControl::FireSubscription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IFiringControl.FireSubscription
---

# IFiringControl::FireSubscription


## -description

Fires an event to a single subscriber.

## -parameters

### -param subscription [in]

A pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a> interface on a subscription object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

The <b>FireSubscription</b> method fires an event to the subscriber associated with the subscription object identified by the <i>subscription</i> parameter. A publisher filter typically iterates through a filtered list of subscriptions and calls <b>FireSubscription</b> for each associated subscriber. All standard delivery processing is done by the event object for the subscription, including the following: 



<ul>
<li>Any standard parameter filtering.
</li>
<li>Activating the subscriber object (optional, for persistent subscriptions).
</li>
<li>Depending on parameter filtering, invoking the event method that originally caused entry into the publisher filter on the subscriber.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ifiringcontrol">IFiringControl</a>