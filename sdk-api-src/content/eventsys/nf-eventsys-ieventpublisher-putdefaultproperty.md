---
UID: NF:eventsys.IEventPublisher.PutDefaultProperty
title: IEventPublisher::PutDefaultProperty (eventsys.h)
description: Writes a named property and its value to the property bag associated with the event publisher.
helpviewer_keywords: ["IEventPublisher interface [COM]","PutDefaultProperty method","IEventPublisher.PutDefaultProperty","IEventPublisher::PutDefaultProperty","PutDefaultProperty","PutDefaultProperty method [COM]","PutDefaultProperty method [COM]","IEventPublisher interface","_com_ieventpublisher_putdefaultproperty","com.ieventpublisher_putdefaultproperty","eventsys/IEventPublisher::PutDefaultProperty"]
old-location: com\ieventpublisher_putdefaultproperty.htm
tech.root: com
ms.assetid: 418f1c16-1b21-4023-b0fc-6e9082b8264e
ms.date: 12/05/2018
ms.keywords: IEventPublisher interface [COM],PutDefaultProperty method, IEventPublisher.PutDefaultProperty, IEventPublisher::PutDefaultProperty, PutDefaultProperty, PutDefaultProperty method [COM], PutDefaultProperty method [COM],IEventPublisher interface, _com_ieventpublisher_putdefaultproperty, com.ieventpublisher_putdefaultproperty, eventsys/IEventPublisher::PutDefaultProperty
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
 - IEventPublisher::PutDefaultProperty
 - eventsys/IEventPublisher::PutDefaultProperty
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
 - IEventPublisher.PutDefaultProperty
---

# IEventPublisher::PutDefaultProperty


## -description

Writes a named property and its value to the property bag associated with the event publisher.

## -parameters

### -param bstrPropertyName [in]

The name of the property whose value is to be set.

### -param propertyValue [in]

The new value for the property.

## -returns

The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

An <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">IEventPublisher</a>