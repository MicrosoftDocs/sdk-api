---
UID: NF:eventsys.IEventSubscription.get_SubscriberCLSID
title: IEventSubscription::get_SubscriberCLSID (eventsys.h)
author: windows-sdk-content
description: The CLSID of the subscriber component (for a persistent subscription).
old-location: cos\ieventsubscription_subscriberclsid.htm
tech.root: cossdk
ms.assetid: 004f662c-8fcb-4490-897b-48bf5ea306c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventSubscription interface [COM+],SubscriberCLSID property, IEventSubscription.SubscriberCLSID, IEventSubscription.get_SubscriberCLSID, IEventSubscription::SubscriberCLSID, IEventSubscription::get_SubscriberCLSID, IEventSubscription::put_SubscriberCLSID, SubscriberCLSID property [COM+], SubscriberCLSID property [COM+],IEventSubscription interface, cos.ieventsubscription_subscriberclsid, eventsys/IEventSubscription::SubscriberCLSID, eventsys/IEventSubscription::get_SubscriberCLSID, eventsys/IEventSubscription::put_SubscriberCLSID, get_SubscriberCLSID
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
 - IEventSubscription.SubscriberCLSID
 - IEventSubscription.get_SubscriberCLSID
 - IEventSubscription.put_SubscriberCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSubscription::get_SubscriberCLSID


## -description


The CLSID of the subscriber component (for a persistent subscription).

This property is read/write.


## -parameters


## -remarks



If not empty, the subscription is persistent and the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberinterface">SubscriberInterface</a> property must be <b>NULL</b>. This property works in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_machinename">MachineName</a> property in a persistent subscription.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>
 

 

