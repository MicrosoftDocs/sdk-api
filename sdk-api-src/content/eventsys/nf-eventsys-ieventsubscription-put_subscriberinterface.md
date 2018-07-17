---
UID: NF:eventsys.IEventSubscription.put_SubscriberInterface
title: IEventSubscription::put_SubscriberInterface
author: windows-sdk-content
description: A marshaled pointer to the event interface on the subscriber (for a transient subscription).
old-location: cos\ieventsubscription_subscriberinterface.htm
old-project: cossdk
ms.assetid: 207c8e74-d8f8-4576-8f2d-762c97bc048f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEventSubscription interface [COM+],SubscriberInterface property, IEventSubscription.SubscriberInterface, IEventSubscription.put_SubscriberInterface, IEventSubscription::SubscriberInterface, IEventSubscription::get_SubscriberInterface, IEventSubscription::put_SubscriberInterface, SubscriberInterface property [COM+], SubscriberInterface property [COM+],IEventSubscription interface, cos.ieventsubscription_subscriberinterface, eventsys/IEventSubscription::SubscriberInterface, eventsys/IEventSubscription::get_SubscriberInterface, eventsys/IEventSubscription::put_SubscriberInterface, put_SubscriberInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: EOC_ChangeType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::put_SubscriberInterface


## -description


A marshaled pointer to the event interface on the subscriber (for a transient subscription).

This property is read/write.


## -parameters


## -remarks



If not <b>NULL</b>, the subscription is transient and the <a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a> property must be empty.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
 

 

