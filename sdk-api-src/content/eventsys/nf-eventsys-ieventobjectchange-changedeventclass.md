---
UID: NF:eventsys.IEventObjectChange.ChangedEventClass
title: IEventObjectChange::ChangedEventClass (eventsys.h)
description: Indicates that an event class object has been added, modified, or deleted. (IEventObjectChange.ChangedEventClass)
helpviewer_keywords: ["ChangedEventClass","ChangedEventClass method [COM+]","ChangedEventClass method [COM+]","IEventObjectChange interface","IEventObjectChange interface [COM+]","ChangedEventClass method","IEventObjectChange.ChangedEventClass","IEventObjectChange::ChangedEventClass","_cos_IEventObjectChange_ChangedEventClass","cos.ieventobjectchange_changedeventclass","eventsys/IEventObjectChange::ChangedEventClass"]
old-location: cos\ieventobjectchange_changedeventclass.htm
tech.root: cos
ms.assetid: 8db711c8-7c01-4fb0-975c-a66c83063124
ms.date: 12/05/2018
ms.keywords: ChangedEventClass, ChangedEventClass method [COM+], ChangedEventClass method [COM+],IEventObjectChange interface, IEventObjectChange interface [COM+],ChangedEventClass method, IEventObjectChange.ChangedEventClass, IEventObjectChange::ChangedEventClass, _cos_IEventObjectChange_ChangedEventClass, cos.ieventobjectchange_changedeventclass, eventsys/IEventObjectChange::ChangedEventClass
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
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
 - IEventObjectChange::ChangedEventClass
 - eventsys/IEventObjectChange::ChangedEventClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEventObjectChange.ChangedEventClass
---

# IEventObjectChange::ChangedEventClass


## -description

Indicates that an event class object has been added, modified, or deleted.

## -parameters

### -param changeType [in]

The type of change to the event class object. Values are taken from the <a href="/windows/desktop/api/eventsys/ne-eventsys-eoc_changetype">EOC_ChangeType</a> enumeration.

### -param bstrEventClassID [in]

The EventClassID property of the event class object that changed.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange">IEventObjectChange</a>
