---
UID: NF:eventsys.IEventObjectChange.ChangedPublisher
title: IEventObjectChange::ChangedPublisher (eventsys.h)
description: Indicates a publisher object has been added, modified, or deleted.
helpviewer_keywords: ["ChangedPublisher","ChangedPublisher method [COM+]","ChangedPublisher method [COM+]","IEventObjectChange interface","IEventObjectChange interface [COM+]","ChangedPublisher method","IEventObjectChange.ChangedPublisher","IEventObjectChange::ChangedPublisher","_cos_ieventobjectchange_changedpublisher","cos.ieventobjectchange_changedpublisher","eventsys/IEventObjectChange::ChangedPublisher"]
old-location: cos\ieventobjectchange_changedpublisher.htm
tech.root: cos
ms.assetid: 13bd95e6-5fc2-41e2-9002-67a87f727528
ms.date: 12/05/2018
ms.keywords: ChangedPublisher, ChangedPublisher method [COM+], ChangedPublisher method [COM+],IEventObjectChange interface, IEventObjectChange interface [COM+],ChangedPublisher method, IEventObjectChange.ChangedPublisher, IEventObjectChange::ChangedPublisher, _cos_ieventobjectchange_changedpublisher, cos.ieventobjectchange_changedpublisher, eventsys/IEventObjectChange::ChangedPublisher
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
 - IEventObjectChange::ChangedPublisher
 - eventsys/IEventObjectChange::ChangedPublisher
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
 - IEventObjectChange.ChangedPublisher
---

# IEventObjectChange::ChangedPublisher


## -description

Indicates a publisher object has been added, modified, or deleted.

## -parameters

### -param changeType [in]

The type of change to the publisher object. Values are taken from the <a href="/windows/desktop/api/eventsys/ne-eventsys-eoc_changetype">EOC_ChangeType</a> enumeration.

### -param bstrPublisherID [in]

The PublisherID property of the publisher object that changed.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange">IEventObjectChange</a>