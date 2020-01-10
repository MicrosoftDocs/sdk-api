---
UID: NF:eventsys.IEventSubscription.GetSubscriberProperty
title: IEventSubscription::GetSubscriberProperty (eventsys.h)
description: Retrieves the value of a property stored in the property bag to define subscriber context.
old-location: cos\ieventsubscription_getsubscriberproperty.htm
tech.root: cossdk
ms.assetid: 6e16557a-e4ea-46ae-8285-0446189cea8e
ms.date: 12/05/2018
ms.keywords: GetSubscriberProperty, GetSubscriberProperty method [COM+], GetSubscriberProperty method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetSubscriberProperty method, IEventSubscription.GetSubscriberProperty, IEventSubscription::GetSubscriberProperty, _cos_IEventSubscription_GetSubscriberProperty, cos.ieventsubscription_getsubscriberproperty, eventsys/IEventSubscription::GetSubscriberProperty
f1_keywords:
- eventsys/IEventSubscription.GetSubscriberProperty
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
- IEventSubscription.GetSubscriberProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSubscription::GetSubscriberProperty


## -description


Retrieves the value of a property stored in the property bag to define subscriber context.


## -parameters




### -param bstrPropertyName [in]

The name of the requested property.


### -param propertyValue [out, retval]

The value of the requested property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a>
 

 

