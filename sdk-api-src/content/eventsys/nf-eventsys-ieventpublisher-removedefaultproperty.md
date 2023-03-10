---
UID: NF:eventsys.IEventPublisher.RemoveDefaultProperty
title: IEventPublisher::RemoveDefaultProperty (eventsys.h)
description: Removes a named property and its value from the property bag associated with the event publisher object.
helpviewer_keywords: ["IEventPublisher interface [COM]","RemoveDefaultProperty method","IEventPublisher.RemoveDefaultProperty","IEventPublisher::RemoveDefaultProperty","RemoveDefaultProperty","RemoveDefaultProperty method [COM]","RemoveDefaultProperty method [COM]","IEventPublisher interface","_com_ieventpublisher_removedefaultproperty","com.ieventpublisher_removedefaultproperty","eventsys/IEventPublisher::RemoveDefaultProperty"]
old-location: com\ieventpublisher_removedefaultproperty.htm
tech.root: com
ms.assetid: da691bac-e940-431d-acef-8c29f4a25c70
ms.date: 12/05/2018
ms.keywords: IEventPublisher interface [COM],RemoveDefaultProperty method, IEventPublisher.RemoveDefaultProperty, IEventPublisher::RemoveDefaultProperty, RemoveDefaultProperty, RemoveDefaultProperty method [COM], RemoveDefaultProperty method [COM],IEventPublisher interface, _com_ieventpublisher_removedefaultproperty, com.ieventpublisher_removedefaultproperty, eventsys/IEventPublisher::RemoveDefaultProperty
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
 - IEventPublisher::RemoveDefaultProperty
 - eventsys/IEventPublisher::RemoveDefaultProperty
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
 - IEventPublisher.RemoveDefaultProperty
---

# IEventPublisher::RemoveDefaultProperty


## -description

Removes a named property and its value from the property bag associated with the event publisher object.

## -parameters

### -param bstrPropertyName [in]

The name of the property to be removed.

## -returns

The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

An <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">IEventPublisher</a>