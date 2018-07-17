---
UID: NF:eventsys.IEventSubscription.GetPublisherProperty
title: IEventSubscription::GetPublisherProperty
author: windows-sdk-content
description: Retrieves the value of a property stored in the property bag to define publisher context.
old-location: cos\ieventsubscription_getpublisherproperty.htm
old-project: cossdk
ms.assetid: 7d0c2467-0ab8-4daf-b4ed-befe28d33757
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetPublisherProperty, GetPublisherProperty method [COM+], GetPublisherProperty method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetPublisherProperty method, IEventSubscription.GetPublisherProperty, IEventSubscription::GetPublisherProperty, _cos_IEventSubscription_GetPublisherProperty, cos.ieventsubscription_getpublisherproperty, eventsys/IEventSubscription::GetPublisherProperty
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
 - IEventSubscription.GetPublisherProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSubscription::GetPublisherProperty


## -description


Retrieves the value of a property stored in the property bag to define publisher context.


## -parameters




### -param bstrPropertyName [in]

The name of the requested property.


### -param propertyValue [out, retval]

The value of the requested property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Publisher filters should call this method to obtain filter properties stored by the subscription builder.





## -see-also




<a href="https://msdn.microsoft.com/ce3f9f7e-3d0a-445f-b3db-671ee595aedf">IEventSubscription</a>



<a href="https://msdn.microsoft.com/94f335be-aeb5-4d24-b475-e2aaae2b0a17">PublisherID</a>
 

 

