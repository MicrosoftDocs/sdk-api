---
UID: NF:eventsys.IEventSubscription.GetSubscriberPropertyCollection
title: IEventSubscription::GetSubscriberPropertyCollection (eventsys.h)
description: Retrieves a collection of properties and values stored in the subscriber property bag.
helpviewer_keywords: ["GetSubscriberPropertyCollection","GetSubscriberPropertyCollection method [COM+]","GetSubscriberPropertyCollection method [COM+]","IEventSubscription interface","IEventSubscription interface [COM+]","GetSubscriberPropertyCollection method","IEventSubscription.GetSubscriberPropertyCollection","IEventSubscription::GetSubscriberPropertyCollection","_cos_IEventSubscription_GetSubscriberPropertyCollection","cos.ieventsubscription_getsubscriberpropertycollection","eventsys/IEventSubscription::GetSubscriberPropertyCollection"]
old-location: cos\ieventsubscription_getsubscriberpropertycollection.htm
tech.root: cos
ms.assetid: 33d00424-a285-4953-aa96-be30d3e7da17
ms.date: 12/05/2018
ms.keywords: GetSubscriberPropertyCollection, GetSubscriberPropertyCollection method [COM+], GetSubscriberPropertyCollection method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetSubscriberPropertyCollection method, IEventSubscription.GetSubscriberPropertyCollection, IEventSubscription::GetSubscriberPropertyCollection, _cos_IEventSubscription_GetSubscriberPropertyCollection, cos.ieventsubscription_getsubscriberpropertycollection, eventsys/IEventSubscription::GetSubscriberPropertyCollection
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
 - IEventSubscription::GetSubscriberPropertyCollection
 - eventsys/IEventSubscription::GetSubscriberPropertyCollection
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
 - IEventSubscription.GetSubscriberPropertyCollection
---

# IEventSubscription::GetSubscriberPropertyCollection


## -description

Retrieves a collection of properties and values stored in the subscriber property bag.

## -parameters

### -param collection [out, retval]

Address of a pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a> interface on an event object collection. This parameter cannot be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>