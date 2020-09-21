---
UID: NF:eventsys.IEventPublisher.GetDefaultPropertyCollection
title: IEventPublisher::GetDefaultPropertyCollection (eventsys.h)
description: Creates a collection object that enumerates the properties contained in the property bag associated with the event publisher object.
helpviewer_keywords: ["GetDefaultPropertyCollection","GetDefaultPropertyCollection method [COM]","GetDefaultPropertyCollection method [COM]","IEventPublisher interface","IEventPublisher interface [COM]","GetDefaultPropertyCollection method","IEventPublisher.GetDefaultPropertyCollection","IEventPublisher::GetDefaultPropertyCollection","_com_ieventpublisher_getdefaultpropertycollection","com.ieventpublisher_getdefaultpropertycollection","eventsys/IEventPublisher::GetDefaultPropertyCollection"]
old-location: com\ieventpublisher_getdefaultpropertycollection.htm
tech.root: com
ms.assetid: ca5d116a-b995-4311-9c58-6b957fca6b53
ms.date: 12/05/2018
ms.keywords: GetDefaultPropertyCollection, GetDefaultPropertyCollection method [COM], GetDefaultPropertyCollection method [COM],IEventPublisher interface, IEventPublisher interface [COM],GetDefaultPropertyCollection method, IEventPublisher.GetDefaultPropertyCollection, IEventPublisher::GetDefaultPropertyCollection, _com_ieventpublisher_getdefaultpropertycollection, com.ieventpublisher_getdefaultpropertycollection, eventsys/IEventPublisher::GetDefaultPropertyCollection
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
 - IEventPublisher::GetDefaultPropertyCollection
 - eventsys/IEventPublisher::GetDefaultPropertyCollection
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
 - IEventPublisher.GetDefaultPropertyCollection
---

# IEventPublisher::GetDefaultPropertyCollection


## -description

Creates a collection object that enumerates the properties contained in the property bag associated with the event publisher object.

## -parameters

### -param collection [out, retval]

A pointer to an <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a> interface pointer on an event object collection. This parameter cannot be <b>NULL</b>.

## -returns

The possible return values include E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

An <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">EventPublisher</a> object includes a property bag that can contain name and value pairs. Objects in the event system, including subscribers, can add, modify, and read these properties.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher">IEventPublisher</a>