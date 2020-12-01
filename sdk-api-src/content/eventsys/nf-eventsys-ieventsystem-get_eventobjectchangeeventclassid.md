---
UID: NF:eventsys.IEventSystem.get_EventObjectChangeEventClassID
title: IEventSystem::get_EventObjectChangeEventClassID (eventsys.h)
description: Retrieves the CLSID of an event class object that notifies the caller of changes to the event store.
helpviewer_keywords: ["EventObjectChangeEventClassID property [COM+]","EventObjectChangeEventClassID property [COM+]","IEventSystem interface","IEventSystem interface [COM+]","EventObjectChangeEventClassID property","IEventSystem.EventObjectChangeEventClassID","IEventSystem.get_EventObjectChangeEventClassID","IEventSystem::EventObjectChangeEventClassID","IEventSystem::get_EventObjectChangeEventClassID","_cos_IEventSystem_Properties","cos.ieventsystem_eventobjectchangeeventclassid","eventsys/IEventSystem::EventObjectChangeEventClassID","eventsys/IEventSystem::get_EventObjectChangeEventClassID","get_EventObjectChangeEventClassID"]
old-location: cos\ieventsystem_eventobjectchangeeventclassid.htm
tech.root: cos
ms.assetid: 58cd529d-f1e5-4777-9999-3f223d27dc64
ms.date: 12/05/2018
ms.keywords: EventObjectChangeEventClassID property [COM+], EventObjectChangeEventClassID property [COM+],IEventSystem interface, IEventSystem interface [COM+],EventObjectChangeEventClassID property, IEventSystem.EventObjectChangeEventClassID, IEventSystem.get_EventObjectChangeEventClassID, IEventSystem::EventObjectChangeEventClassID, IEventSystem::get_EventObjectChangeEventClassID, _cos_IEventSystem_Properties, cos.ieventsystem_eventobjectchangeeventclassid, eventsys/IEventSystem::EventObjectChangeEventClassID, eventsys/IEventSystem::get_EventObjectChangeEventClassID, get_EventObjectChangeEventClassID
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
 - IEventSystem::get_EventObjectChangeEventClassID
 - eventsys/IEventSystem::get_EventObjectChangeEventClassID
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
 - IEventSystem.EventObjectChangeEventClassID
 - IEventSystem.get_EventObjectChangeEventClassID
---

# IEventSystem::get_EventObjectChangeEventClassID


## -description

Retrieves the CLSID of an event class object that notifies the caller of changes to the event store.

This property is read-only.

## -parameters

## -remarks

Subscriptions can use the <b>EventObjectChangeEventClassID</b> property to obtain a pointer to an event class object that notifies them when subscribers or events are modified or when they are added to or deleted from the event store. Subscribers to these events must implement the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange">IEventObjectChange</a> interface.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a>