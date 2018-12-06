---
UID: NF:eventsys.IEventSubscription.GetSubscriberProperty
title: IEventSubscription::GetSubscriberProperty
author: windows-sdk-content
description: Retrieves the value of a property stored in the property bag to define subscriber context.
old-location: cos\ieventsubscription_getsubscriberproperty.htm
tech.root: cossdk
ms.assetid: 6e16557a-e4ea-46ae-8285-0446189cea8e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSubscriberProperty, GetSubscriberProperty method [COM+], GetSubscriberProperty method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetSubscriberProperty method, IEventSubscription.GetSubscriberProperty, IEventSubscription::GetSubscriberProperty, _cos_IEventSubscription_GetSubscriberProperty, cos.ieventsubscription_getsubscriberproperty, eventsys/IEventSubscription::GetSubscriberProperty
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
 - IEventSubscription.GetSubscriberProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>



<a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a>
 

 

