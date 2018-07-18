---
UID: NF:eventsys.IEventSubscription.PutPublisherProperty
title: IEventSubscription::PutPublisherProperty
author: windows-sdk-content
description: Writes a property and its value to the property bag to define publisher context.
old-location: cos\ieventsubscription_putpublisherproperty.htm
old-project: cossdk
ms.assetid: af8ae243-d28b-4909-a4e8-98ffe336fc9a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IEventSubscription interface [COM+],PutPublisherProperty method, IEventSubscription.PutPublisherProperty, IEventSubscription::PutPublisherProperty, PutPublisherProperty, PutPublisherProperty method [COM+], PutPublisherProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_PutPublisherProperty, cos.ieventsubscription_putpublisherproperty, eventsys/IEventSubscription::PutPublisherProperty
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
 - IEventSubscription.PutPublisherProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::PutPublisherProperty


## -description


Writes a property and its value to the property bag to define publisher context.


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



<a href="https://msdn.microsoft.com/94f335be-aeb5-4d24-b475-e2aaae2b0a17">PublisherID</a>
 

 

