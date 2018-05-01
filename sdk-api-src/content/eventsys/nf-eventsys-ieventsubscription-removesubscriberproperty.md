---
UID: NF:eventsys.IEventSubscription.RemoveSubscriberProperty
title: IEventSubscription::RemoveSubscriberProperty method
author: windows-driver-content
description: Removes a property and its value from the property bag that defines subscriber context.
old-location: cos\ieventsubscription_removesubscriberproperty.htm
old-project: cossdk
ms.assetid: 3c0cd763-8528-4f8b-8a09-c36860cad9b7
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IEventSubscription, IEventSubscription interface [COM+], RemoveSubscriberProperty method, IEventSubscription::RemoveSubscriberProperty, RemoveSubscriberProperty method [COM+], RemoveSubscriberProperty method [COM+], IEventSubscription interface, RemoveSubscriberProperty,IEventSubscription.RemoveSubscriberProperty, _cos_IEventSubscription_RemoveSubscriberProperty, cos.ieventsubscription_removesubscriberproperty, eventsys/IEventSubscription::RemoveSubscriberProperty
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IEventSubscription.RemoveSubscriberProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::RemoveSubscriberProperty method


## -description


Removes a property and its value from the property bag that defines subscriber context.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be removed from the property bag. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>



<a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a>
 

 

