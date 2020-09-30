---
UID: NF:eventsys.IEventPublisher.GetDefaultProperty
title: IEventPublisher::GetDefaultProperty (eventsys.h)
description: Retrieves a named property and its value from the property bag associated with the event publisher.
helpviewer_keywords: ["GetDefaultProperty","GetDefaultProperty method [COM]","GetDefaultProperty method [COM]","IEventPublisher interface","IEventPublisher interface [COM]","GetDefaultProperty method","IEventPublisher.GetDefaultProperty","IEventPublisher::GetDefaultProperty","_com_ieventpublisher_getdefaultproperty","com.ieventpublisher_getdefaultproperty","eventsys/IEventPublisher::GetDefaultProperty"]
old-location: com\ieventpublisher_getdefaultproperty.htm
tech.root: com
ms.assetid: 5d9adc4f-30c9-42bd-89c9-e35384885b8c
ms.date: 12/05/2018
ms.keywords: GetDefaultProperty, GetDefaultProperty method [COM], GetDefaultProperty method [COM],IEventPublisher interface, IEventPublisher interface [COM],GetDefaultProperty method, IEventPublisher.GetDefaultProperty, IEventPublisher::GetDefaultProperty, _com_ieventpublisher_getdefaultproperty, com.ieventpublisher_getdefaultproperty, eventsys/IEventPublisher::GetDefaultProperty
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
 - IEventPublisher::GetDefaultProperty
 - eventsys/IEventPublisher::GetDefaultProperty
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
 - IEventPublisher.GetDefaultProperty
---

# IEventPublisher::GetDefaultProperty


## -description

Retrieves a named property and its value from the property bag associated with the event publisher.

## -parameters

### -param bstrPropertyName [in]

The name of the property whose value is to be retrieved.

### -param propertyValue [out, retval]

A pointer to the variable that receives the property.

## -returns

The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

An <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">IEventPublisher</a>