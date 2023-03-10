---
UID: NF:eventsys.IEventObjectCollection.Remove
title: IEventObjectCollection::Remove (eventsys.h)
description: Removes an event object from the collection.
helpviewer_keywords: ["IEventObjectCollection interface [COM+]","Remove method","IEventObjectCollection.Remove","IEventObjectCollection::Remove","Remove","Remove method [COM+]","Remove method [COM+]","IEventObjectCollection interface","_cos_IEventObjectCollection_Remove","cos.ieventobjectcollection_remove","eventsys/IEventObjectCollection::Remove"]
old-location: cos\ieventobjectcollection_remove.htm
tech.root: cos
ms.assetid: 5092b1e1-bbf2-493c-92be-41196b43d4f2
ms.date: 12/05/2018
ms.keywords: IEventObjectCollection interface [COM+],Remove method, IEventObjectCollection.Remove, IEventObjectCollection::Remove, Remove, Remove method [COM+], Remove method [COM+],IEventObjectCollection interface, _cos_IEventObjectCollection_Remove, cos.ieventobjectcollection_remove, eventsys/IEventObjectCollection::Remove
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
 - IEventObjectCollection::Remove
 - eventsys/IEventObjectCollection::Remove
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
 - IEventObjectCollection.Remove
---

# IEventObjectCollection::Remove


## -description

Removes an event object from the collection.

## -parameters

### -param objectID [in]

The ID property of the event object to be removed. For example, if the collection consists of subscription objects, this parameter would contain the SubscriptionID property of the event subscription object to be removed from the collection.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a>