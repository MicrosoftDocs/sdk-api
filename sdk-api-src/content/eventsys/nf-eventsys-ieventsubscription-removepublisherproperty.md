---
UID: NF:eventsys.IEventSubscription.RemovePublisherProperty
title: IEventSubscription::RemovePublisherProperty
author: windows-sdk-content
description: Removes a property and its value from the property bag that defines publisher context.
old-location: cos\ieventsubscription_removepublisherproperty.htm
old-project: cossdk
ms.assetid: 3893e605-dd01-47d3-bb7d-095964433ef9
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IEventSubscription interface [COM+],RemovePublisherProperty method, IEventSubscription.RemovePublisherProperty, IEventSubscription::RemovePublisherProperty, RemovePublisherProperty, RemovePublisherProperty method [COM+], RemovePublisherProperty method [COM+],IEventSubscription interface, _cos_IEventSubscription_RemovePublisherProperty, cos.ieventsubscription_removepublisherproperty, eventsys/IEventSubscription::RemovePublisherProperty
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
 - IEventSubscription.RemovePublisherProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::RemovePublisherProperty


## -description


Removes a property and its value from the property bag that defines publisher context.


## -parameters




### -param bstrPropertyName [in]

The name of the property whose value is to be removed from the property bag. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



A property bag is used to store information about the events the subscriber needs to be notified about. For example, if a subscriber to a sports ticker is to obtain only baseball scores, it could use the property bag in the subscription object to specify this restriction.




## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>



<a href="https://msdn.microsoft.com/94f335be-aeb5-4d24-b475-e2aaae2b0a17">PublisherID</a>
 

 

