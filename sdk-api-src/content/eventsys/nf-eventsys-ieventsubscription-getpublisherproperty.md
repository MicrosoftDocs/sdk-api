---
UID: NF:eventsys.IEventSubscription.GetPublisherProperty
title: IEventSubscription::GetPublisherProperty (eventsys.h)
description: Retrieves the value of a property stored in the property bag to define publisher context.
helpviewer_keywords: ["GetPublisherProperty","GetPublisherProperty method [COM+]","GetPublisherProperty method [COM+]","IEventSubscription interface","IEventSubscription interface [COM+]","GetPublisherProperty method","IEventSubscription.GetPublisherProperty","IEventSubscription::GetPublisherProperty","_cos_IEventSubscription_GetPublisherProperty","cos.ieventsubscription_getpublisherproperty","eventsys/IEventSubscription::GetPublisherProperty"]
old-location: cos\ieventsubscription_getpublisherproperty.htm
tech.root: cos
ms.assetid: 7d0c2467-0ab8-4daf-b4ed-befe28d33757
ms.date: 12/05/2018
ms.keywords: GetPublisherProperty, GetPublisherProperty method [COM+], GetPublisherProperty method [COM+],IEventSubscription interface, IEventSubscription interface [COM+],GetPublisherProperty method, IEventSubscription.GetPublisherProperty, IEventSubscription::GetPublisherProperty, _cos_IEventSubscription_GetPublisherProperty, cos.ieventsubscription_getpublisherproperty, eventsys/IEventSubscription::GetPublisherProperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEventSubscription::GetPublisherProperty
 - eventsys/IEventSubscription::GetPublisherProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IEventSubscription.GetPublisherProperty
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

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a>



<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_publisherid">PublisherID</a>