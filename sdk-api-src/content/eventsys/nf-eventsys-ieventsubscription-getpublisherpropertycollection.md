---
UID: NF:eventsys.IEventSubscription.GetPublisherPropertyCollection
title: IEventSubscription::GetPublisherPropertyCollection (eventsys.h)
description: Retrieves a collection of properties and values stored in the publisher property bag.
helpviewer_keywords: ["GetPublisherPropertyCollection","GetPublisherPropertyCollection method [COM+]","GetPublisherPropertyCollection method [COM+]","IEventSubscription interface","IEventSubscription interface [COM+]","GetPublisherPropertyCollection method","IEventSubscription.GetPublisherPropertyCollection","IEventSubscription::GetPublisherPropertyCollection","_cos_IEventSubscription_GetPublisherPropertyCollection","cos.ieventsubscription_getpublisherpropertycollection","eventsys/IEventSubscription::GetPublisherPropertyCollection"]
old-location: cos\ieventsubscription_getpublisherpropertycollection.htm
tech.root: cos
ms.assetid: d59b46bc-cfc4-400b-8b91-6d0f68f8d9b3
ms.date: 12/05/2018
ms.keywords: GetPublisherPropertyCollection, GetPublisherPropertyCollection method [COM+], GetPublisherPropertyCollection method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetPublisherPropertyCollection method, IEventSubscription.GetPublisherPropertyCollection, IEventSubscription::GetPublisherPropertyCollection, _cos_IEventSubscription_GetPublisherPropertyCollection, cos.ieventsubscription_getpublisherpropertycollection, eventsys/IEventSubscription::GetPublisherPropertyCollection
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
 - IEventSubscription::GetPublisherPropertyCollection
 - eventsys/IEventSubscription::GetPublisherPropertyCollection
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
 - IEventSubscription.GetPublisherPropertyCollection
---

# IEventSubscription::GetPublisherPropertyCollection


## -description

Retrieves a collection of properties and values stored in the publisher property bag.

## -parameters

### -param collection [out, retval]

Address of a pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a> interface on an event object collection. This parameter cannot be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>