---
UID: NF:eventsys.IEventObjectChange2.ChangedEventClass
title: IEventObjectChange2::ChangedEventClass (eventsys.h)
description: Indicates that an event class object has been added, modified, or deleted. (IEventObjectChange2.ChangedEventClass)
helpviewer_keywords: ["ChangedEventClass","ChangedEventClass method [COM+]","ChangedEventClass method [COM+]","IEventObjectChange2 interface","IEventObjectChange2 interface [COM+]","ChangedEventClass method","IEventObjectChange2.ChangedEventClass","IEventObjectChange2::ChangedEventClass","_cos_ieventobjectchange2_changedeventclass","cos.ieventobjectchange2_changedeventclass","eventsys/IEventObjectChange2::ChangedEventClass"]
old-location: cos\ieventobjectchange2_changedeventclass.htm
tech.root: cos
ms.assetid: ae760225-2c4f-46e5-8d35-eefec8f2f5da
ms.date: 12/05/2018
ms.keywords: ChangedEventClass, ChangedEventClass method [COM+], ChangedEventClass method [COM+],IEventObjectChange2 interface, IEventObjectChange2 interface [COM+],ChangedEventClass method, IEventObjectChange2.ChangedEventClass, IEventObjectChange2::ChangedEventClass, _cos_ieventobjectchange2_changedeventclass, cos.ieventobjectchange2_changedeventclass, eventsys/IEventObjectChange2::ChangedEventClass
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
 - IEventObjectChange2::ChangedEventClass
 - eventsys/IEventObjectChange2::ChangedEventClass
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
 - IEventObjectChange2.ChangedEventClass
---

# IEventObjectChange2::ChangedEventClass


## -description

Indicates that an event class object has been added, modified, or deleted.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/eventsys/ns-eventsys-comeventsyschangeinfo">COMEVENTSYSCHANGEINFO</a> structure.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange2">IEventObjectChange2</a>
