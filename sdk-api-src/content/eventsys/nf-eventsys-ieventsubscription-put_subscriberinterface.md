---
UID: NF:eventsys.IEventSubscription.put_SubscriberInterface
title: IEventSubscription::put_SubscriberInterface (eventsys.h)

description: A marshaled pointer to the event interface on the subscriber (for a transient subscription).
old-location: cos\ieventsubscription_subscriberinterface.htm
tech.root: cossdk
ms.assetid: 207c8e74-d8f8-4576-8f2d-762c97bc048f

ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],SubscriberInterface property, IEventSubscription.SubscriberInterface, IEventSubscription.put_SubscriberInterface, IEventSubscription::SubscriberInterface, IEventSubscription::get_SubscriberInterface, IEventSubscription::put_SubscriberInterface, SubscriberInterface property [COM+], SubscriberInterface property [COM+],IEventSubscription interface, cos.ieventsubscription_subscriberinterface, eventsys/IEventSubscription::SubscriberInterface, eventsys/IEventSubscription::get_SubscriberInterface, eventsys/IEventSubscription::put_SubscriberInterface, put_SubscriberInterface
ms.topic: method
f1_keywords: 
 - "eventsys/IEventSubscription.SubscriberInterface"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSubscription::put_SubscriberInterface


## -description


A marshaled pointer to the event interface on the subscriber (for a transient subscription).

This property is read/write.


## -parameters


## -remarks



If not <b>NULL</b>, the subscription is transient and the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a> property must be empty.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
 

 

