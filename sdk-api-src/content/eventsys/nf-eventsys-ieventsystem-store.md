---
UID: NF:eventsys.IEventSystem.Store
title: IEventSystem::Store (eventsys.h)
description: Creates or modifies an event or subscription object within the event system.
helpviewer_keywords: ["IEventSystem interface [COM+]","Store method","IEventSystem.Store","IEventSystem::Store","Store","Store method [COM+]","Store method [COM+]","IEventSystem interface","_cos_IEventSystem_Store","cos.ieventsystem_store","eventsys/IEventSystem::Store"]
old-location: cos\ieventsystem_store.htm
tech.root: cos
ms.assetid: a9999ba1-9ae1-4fc0-9613-be31961fb514
ms.date: 12/05/2018
ms.keywords: IEventSystem interface [COM+],Store method, IEventSystem.Store, IEventSystem::Store, Store, Store method [COM+], Store method [COM+],IEventSystem interface, _cos_IEventSystem_Store, cos.ieventsystem_store, eventsys/IEventSystem::Store
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
 - IEventSystem::Store
 - eventsys/IEventSystem::Store
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
 - IEventSystem.Store
---

# IEventSystem::Store


## -description

Creates or modifies an event or subscription object within the event system.

## -parameters

### -param ProgID [in]

The ProgID of the event object to be added. This must be a valid event object class identifier. The possible values are PROGID_EventSubscription and PROGID_EventClass.

### -param pInterface [in]

A pointer to the object to be added. Depending on the object specified by the <i>ProgID</i> parameter, this is a pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsubscription">IEventSubscription</a> or <a href="/windows/desktop/api/eventsys/nn-eventsys-ieventclass">IEventClass</a> interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EVENT_E_INVALID_PER_USER_SID</b></dt>
</dl>
</td>
<td width="60%">
The owner SID on a per-user subscription does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a>