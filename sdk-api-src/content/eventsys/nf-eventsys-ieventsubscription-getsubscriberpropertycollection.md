---
UID: NF:eventsys.IEventSubscription.GetSubscriberPropertyCollection
title: IEventSubscription::GetSubscriberPropertyCollection
author: windows-sdk-content
description: Retrieves a collection of properties and values stored in the subscriber property bag.
old-location: cos\ieventsubscription_getsubscriberpropertycollection.htm
tech.root: cossdk
ms.assetid: 33d00424-a285-4953-aa96-be30d3e7da17
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetSubscriberPropertyCollection, GetSubscriberPropertyCollection method [COM+], GetSubscriberPropertyCollection method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetSubscriberPropertyCollection method, IEventSubscription.GetSubscriberPropertyCollection, IEventSubscription::GetSubscriberPropertyCollection, _cos_IEventSubscription_GetSubscriberPropertyCollection, cos.ieventsubscription_getsubscriberpropertycollection, eventsys/IEventSubscription::GetSubscriberPropertyCollection
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
 - IEventSubscription.GetSubscriberPropertyCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventSubscription::GetSubscriberPropertyCollection


## -description


Retrieves a collection of properties and values stored in the subscriber property bag.


## -parameters




### -param collection [out, retval]

Address of a pointer to the <a href="https://msdn.microsoft.com/7bb00b80-a48f-49c8-983d-9ff0ea424e4d">IEventObjectCollection</a> interface on an event object collection. This parameter cannot be <b>NULL</b>. 


## -returns



This method can return the standard return values E_INVALIDARG, E_POINTER, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction. 





## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>
 

 

