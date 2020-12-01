---
UID: NF:eventsys.IEventSubscription.RemovePublisherProperty
title: IEventSubscription::RemovePublisherProperty (eventsys.h)
description: Removes a property and its value from the property bag that defines publisher context.
helpviewer_keywords: ["IEventSubscription interface [COM+]","RemovePublisherProperty method","IEventSubscription.RemovePublisherProperty","IEventSubscription::RemovePublisherProperty","RemovePublisherProperty","RemovePublisherProperty method [COM+]","RemovePublisherProperty method [COM+]","IEventSubscription interface","_cos_IEventSubscription_RemovePublisherProperty","cos.ieventsubscription_removepublisherproperty","eventsys/IEventSubscription::RemovePublisherProperty"]
old-location: cos\ieventsubscription_removepublisherproperty.htm
tech.root: cos
ms.assetid: 3893e605-dd01-47d3-bb7d-095964433ef9
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],RemovePublisherProperty method, IEventSubscription.RemovePublisherProperty, IEventSubscription::RemovePublisherProperty, RemovePublisherProperty, RemovePublisherProperty method [COM+], RemovePublisherProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_RemovePublisherProperty, cos.ieventsubscription_removepublisherproperty, eventsys/IEventSubscription::RemovePublisherProperty
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
 - IEventSubscription::RemovePublisherProperty
 - eventsys/IEventSubscription::RemovePublisherProperty
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
 - IEventSubscription.RemovePublisherProperty
---

# IEventSubscription::RemovePublisherProperty


## -description

Removes a property and its value from the property bag that defines publisher context.

## -parameters

### -param bstrPropertyName [in]

The name of the property whose value is to be removed from the property bag.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_publisherid">PublisherID</a>