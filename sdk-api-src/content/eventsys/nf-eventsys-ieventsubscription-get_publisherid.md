---
UID: NF:eventsys.IEventSubscription.get_PublisherID
title: IEventSubscription::get_PublisherID (eventsys.h)
description: The unique ID of the event publisher.
helpviewer_keywords: ["IEventSubscription interface [COM+]","PublisherID property","IEventSubscription.PublisherID","IEventSubscription.get_PublisherID","IEventSubscription::PublisherID","IEventSubscription::get_PublisherID","IEventSubscription::put_PublisherID","PublisherID property [COM+]","PublisherID property [COM+]","IEventSubscription interface","cos.ieventsubscription_publisherid","eventsys/IEventSubscription::PublisherID","eventsys/IEventSubscription::get_PublisherID","eventsys/IEventSubscription::put_PublisherID","get_PublisherID"]
old-location: cos\ieventsubscription_publisherid.htm
tech.root: cos
ms.assetid: 94f335be-aeb5-4d24-b475-e2aaae2b0a17
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],PublisherID property, IEventSubscription.PublisherID, IEventSubscription.get_PublisherID, IEventSubscription::PublisherID, IEventSubscription::get_PublisherID, IEventSubscription::put_PublisherID, PublisherID property [COM+], PublisherID property [COM+],IEventSubscription interface, cos.ieventsubscription_publisherid, eventsys/IEventSubscription::PublisherID, eventsys/IEventSubscription::get_PublisherID, eventsys/IEventSubscription::put_PublisherID, get_PublisherID
f1_keywords:
- eventsys/IEventSubscription.PublisherID
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
- IEventSubscription.PublisherID
- IEventSubscription.get_PublisherID
- IEventSubscription.put_PublisherID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSubscription::get_PublisherID


## -description


The unique ID of the event publisher.

This property is read/write.


## -parameters


## -remarks



Specifying a <b>PublisherID</b> property does not guarantee that a subscriber will not receive events fired by other publishers.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
 

 

