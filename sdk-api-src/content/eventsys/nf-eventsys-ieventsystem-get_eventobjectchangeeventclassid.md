---
UID: NF:eventsys.IEventSystem.get_EventObjectChangeEventClassID
title: IEventSystem::get_EventObjectChangeEventClassID method
author: windows-driver-content
description: Retrieves the CLSID of an event class object that notifies the caller of changes to the event store.
old-location: cos\ieventsystem_eventobjectchangeeventclassid.htm
old-project: cossdk
ms.assetid: 58cd529d-f1e5-4777-9999-3f223d27dc64
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EventObjectChangeEventClassID property [COM+], EventObjectChangeEventClassID property [COM+], IEventSystem interface, IEventSystem, IEventSystem interface [COM+], EventObjectChangeEventClassID property, IEventSystem.EventObjectChangeEventClassID, IEventSystem::get_EventObjectChangeEventClassID, _cos_IEventSystem_Properties, cos.ieventsystem_eventobjectchangeeventclassid, eventsys/IEventSystem::EventObjectChangeEventClassID, eventsys/IEventSystem::get_EventObjectChangeEventClassID, get_EventObjectChangeEventClassID,IEventSystem.get_EventObjectChangeEventClassID
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
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EventSys.h
api_name:
-	IEventSystem.EventObjectChangeEventClassID
-	IEventSystem.get_EventObjectChangeEventClassID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSystem::get_EventObjectChangeEventClassID method


## -description


Retrieves the CLSID of an event class object that notifies the caller of changes to the event store.

This property is read-only.


## -parameters


## -remarks



Subscriptions can use the <b>EventObjectChangeEventClassID</b> property to obtain a pointer to an event class object that notifies them when subscribers or events are modified or when they are added to or deleted from the event store. Subscribers to these events must implement the <a href="https://msdn.microsoft.com/2e916601-e03d-4c5f-a8fb-38317cfb66ad">IEventObjectChange</a> interface.





## -see-also




<a href="https://msdn.microsoft.com/29b3e552-b717-4d10-9fa4-1386da3c5460">IEventSystem</a>
 

 

