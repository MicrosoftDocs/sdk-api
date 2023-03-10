---
UID: NF:eventsys.IEventSubscription.RemoveSubscriberProperty
title: IEventSubscription::RemoveSubscriberProperty (eventsys.h)
description: Removes a property and its value from the property bag that defines subscriber context.
helpviewer_keywords: ["IEventSubscription interface [COM+]","RemoveSubscriberProperty method","IEventSubscription.RemoveSubscriberProperty","IEventSubscription::RemoveSubscriberProperty","RemoveSubscriberProperty","RemoveSubscriberProperty method [COM+]","RemoveSubscriberProperty method [COM+]","IEventSubscription interface","_cos_IEventSubscription_RemoveSubscriberProperty","cos.ieventsubscription_removesubscriberproperty","eventsys/IEventSubscription::RemoveSubscriberProperty"]
old-location: cos\ieventsubscription_removesubscriberproperty.htm
tech.root: cos
ms.assetid: 3c0cd763-8528-4f8b-8a09-c36860cad9b7
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],RemoveSubscriberProperty method, IEventSubscription.RemoveSubscriberProperty, IEventSubscription::RemoveSubscriberProperty, RemoveSubscriberProperty, RemoveSubscriberProperty method [COM+], RemoveSubscriberProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_RemoveSubscriberProperty, cos.ieventsubscription_removesubscriberproperty, eventsys/IEventSubscription::RemoveSubscriberProperty
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
 - IEventSubscription::RemoveSubscriberProperty
 - eventsys/IEventSubscription::RemoveSubscriberProperty
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
 - IEventSubscription.RemoveSubscriberProperty
---

# IEventSubscription::RemoveSubscriberProperty


## -description

Removes a property and its value from the property bag that defines subscriber context.

## -parameters

### -param bstrPropertyName [in]

The name of the property whose value is to be removed from the property bag.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a>