---
UID: NF:eventsys.IEnumEventObject.Clone
title: IEnumEventObject::Clone (eventsys.h)
description: Creates an enumerator that contains the same enumeration state as the current one. (IEnumEventObject.Clone)
helpviewer_keywords: ["Clone","Clone method [COM+]","Clone method [COM+]","IEnumEventObject interface","IEnumEventObject interface [COM+]","Clone method","IEnumEventObject.Clone","IEnumEventObject::Clone","_cos_ienumeventobject_clone","cos.ienumeventobject_clone","eventsys/IEnumEventObject::Clone"]
old-location: cos\ienumeventobject_clone.htm
tech.root: cos
ms.assetid: 25bd3f8f-ba99-42e6-b7af-6b237343a17c
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [COM+], Clone method [COM+],IEnumEventObject interface, IEnumEventObject interface [COM+],Clone method, IEnumEventObject.Clone, IEnumEventObject::Clone, _cos_ienumeventobject_clone, cos.ienumeventobject_clone, eventsys/IEnumEventObject::Clone
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
 - IEnumEventObject::Clone
 - eventsys/IEnumEventObject::Clone
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
 - IEnumEventObject.Clone
---

# IEnumEventObject::Clone


## -description

Creates an enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppInterface [out]

Address of a pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a> interface on the enumeration object. This parameter cannot be <b>NULL</b>. If the method is unsuccessful, the value of this output variable is undefined.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

When the pointer to the <a href="/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a> is returned, it is positioned at the first object in the collection not at the place of the enumeration object being cloned.

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a>
