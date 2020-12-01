---
UID: NF:eventsys.IEventSubscription.PutSubscriberProperty
title: IEventSubscription::PutSubscriberProperty (eventsys.h)
description: Writes a property and its value to the property bag to define subscriber context.
helpviewer_keywords: ["IEventSubscription interface [COM+]","PutSubscriberProperty method","IEventSubscription.PutSubscriberProperty","IEventSubscription::PutSubscriberProperty","PutSubscriberProperty","PutSubscriberProperty method [COM+]","PutSubscriberProperty method [COM+]","IEventSubscription interface","_cos_IEventSubscription_PutSubscriberProperty","cos.ieventsubscription_putsubscriberproperty","eventsys/IEventSubscription::PutSubscriberProperty"]
old-location: cos\ieventsubscription_putsubscriberproperty.htm
tech.root: cos
ms.assetid: 817ee07c-32ea-41a4-a871-370c06bfc8a8
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],PutSubscriberProperty method, IEventSubscription.PutSubscriberProperty, IEventSubscription::PutSubscriberProperty, PutSubscriberProperty, PutSubscriberProperty method [COM+], PutSubscriberProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_PutSubscriberProperty, cos.ieventsubscription_putsubscriberproperty, eventsys/IEventSubscription::PutSubscriberProperty
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
 - IEventSubscription::PutSubscriberProperty
 - eventsys/IEventSubscription::PutSubscriberProperty
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
 - IEventSubscription.PutSubscriberProperty
---

# IEventSubscription::PutSubscriberProperty


## -description

Writes a property and its value to the property bag to define subscriber context.

## -parameters

### -param bstrPropertyName [in]

The name of the property whose value is to be written to the property bag. If the property is not in the property bag, this method adds it.

### -param propertyValue [in]

The value of the property to be written to the property bag. If the property is already in the property bag, this method overwrites the current value.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a>