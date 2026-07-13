---
UID: NF:eventsys.IEventObjectChange2.ChangedSubscription
title: IEventObjectChange2::ChangedSubscription (eventsys.h)
description: Indicates that a subscription object has been added, modified, or deleted. (IEventObjectChange2.ChangedSubscription)
helpviewer_keywords: ["ChangedSubscription","ChangedSubscription method [COM+]","ChangedSubscription method [COM+]","IEventObjectChange2 interface","IEventObjectChange2 interface [COM+]","ChangedSubscription method","IEventObjectChange2.ChangedSubscription","IEventObjectChange2::ChangedSubscription","_cos_ieventobjectchange2_changedsubscription","cos.ieventobjectchange2_changedsubscription","eventsys/IEventObjectChange2::ChangedSubscription"]
old-location: cos\ieventobjectchange2_changedsubscription.htm
tech.root: cos
ms.assetid: 848d5af0-53aa-4ba4-9b21-0caf8e85d01d
ms.date: 12/05/2018
ms.keywords: ChangedSubscription, ChangedSubscription method [COM+], ChangedSubscription method [COM+],IEventObjectChange2 interface, IEventObjectChange2 interface [COM+],ChangedSubscription method, IEventObjectChange2.ChangedSubscription, IEventObjectChange2::ChangedSubscription, _cos_ieventobjectchange2_changedsubscription, cos.ieventobjectchange2_changedsubscription, eventsys/IEventObjectChange2::ChangedSubscription
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
 - IEventObjectChange2::ChangedSubscription
 - eventsys/IEventObjectChange2::ChangedSubscription
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
 - IEventObjectChange2.ChangedSubscription
---

# IEventObjectChange2::ChangedSubscription


## -description

Indicates that a subscription object has been added, modified, or deleted.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/eventsys/ns-eventsys-comeventsyschangeinfo">COMEVENTSYSCHANGEINFO</a> structure.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange2">IEventObjectChange2</a>
