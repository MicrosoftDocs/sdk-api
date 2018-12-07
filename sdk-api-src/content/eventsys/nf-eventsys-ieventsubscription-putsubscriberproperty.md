---
UID: NF:eventsys.IEventSubscription.PutSubscriberProperty
title: IEventSubscription::PutSubscriberProperty
author: windows-sdk-content
description: Writes a property and its value to the property bag to define subscriber context.
old-location: cos\ieventsubscription_putsubscriberproperty.htm
tech.root: cossdk
ms.assetid: 817ee07c-32ea-41a4-a871-370c06bfc8a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEventSubscription interface [COM+],PutSubscriberProperty method, IEventSubscription.PutSubscriberProperty, IEventSubscription::PutSubscriberProperty, PutSubscriberProperty, PutSubscriberProperty method [COM+], PutSubscriberProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_PutSubscriberProperty, cos.ieventsubscription_putsubscriberproperty, eventsys/IEventSubscription::PutSubscriberProperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IEventSubscription.PutSubscriberProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventSubscription::PutSubscriberProperty


## -description


Writes a property and its value to the property bag to define subscriber context.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be written to the property bag. If the property is not in the property bag, this method adds it. 


### -param propertyValue [in]

The value of the property to be written to the property bag. If the property is already in the property bag, this method overwrites the current value. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction. 





## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>



<a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a>
 

 

