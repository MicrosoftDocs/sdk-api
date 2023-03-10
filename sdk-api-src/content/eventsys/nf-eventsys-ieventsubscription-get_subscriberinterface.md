---
UID: NF:eventsys.IEventSubscription.get_SubscriberInterface
title: IEventSubscription::get_SubscriberInterface (eventsys.h)
description: A marshaled pointer to the event interface on the subscriber (for a transient subscription). (Get)
helpviewer_keywords: ["IEventSubscription interface [COM+]","SubscriberInterface property","IEventSubscription.SubscriberInterface","IEventSubscription.get_SubscriberInterface","IEventSubscription::SubscriberInterface","IEventSubscription::get_SubscriberInterface","IEventSubscription::put_SubscriberInterface","SubscriberInterface property [COM+]","SubscriberInterface property [COM+]","IEventSubscription interface","cos.ieventsubscription_subscriberinterface","eventsys/IEventSubscription::SubscriberInterface","eventsys/IEventSubscription::get_SubscriberInterface","eventsys/IEventSubscription::put_SubscriberInterface","get_SubscriberInterface"]
old-location: cos\ieventsubscription_subscriberinterface.htm
tech.root: cos
ms.assetid: 207c8e74-d8f8-4576-8f2d-762c97bc048f
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],SubscriberInterface property, IEventSubscription.SubscriberInterface, IEventSubscription.get_SubscriberInterface, IEventSubscription::SubscriberInterface, IEventSubscription::get_SubscriberInterface, IEventSubscription::put_SubscriberInterface, SubscriberInterface property [COM+], SubscriberInterface property [COM+],IEventSubscription interface, cos.ieventsubscription_subscriberinterface, eventsys/IEventSubscription::SubscriberInterface, eventsys/IEventSubscription::get_SubscriberInterface, eventsys/IEventSubscription::put_SubscriberInterface, get_SubscriberInterface
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
 - IEventSubscription::get_SubscriberInterface
 - eventsys/IEventSubscription::get_SubscriberInterface
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
 - IEventSubscription.SubscriberInterface
 - IEventSubscription.get_SubscriberInterface
 - IEventSubscription.put_SubscriberInterface
---

# IEventSubscription::get_SubscriberInterface


## -description

A marshaled pointer to the event interface on the subscriber (for a transient subscription).

This property is read/write.

## -parameters

## -remarks

If not <b>NULL</b>, the subscription is transient and the <a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a> property must be empty.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
