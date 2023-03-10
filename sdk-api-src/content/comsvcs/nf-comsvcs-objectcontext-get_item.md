---
UID: NF:comsvcs.ObjectContext.get_Item
title: ObjectContext::get_Item (comsvcs.h)
description: Retrieves a named property.
helpviewer_keywords: ["ObjectContext interface [COM+]","get_Item method","ObjectContext.get_Item","ObjectContext::get_Item","_cos_ObjectContext_get_Item","comsvcs/ObjectContext::get_Item","cos.objectcontext_get_item","get_Item","get_Item method [COM+]","get_Item method [COM+]","ObjectContext interface"]
old-location: cos\objectcontext_get_item.htm
tech.root: cos
ms.assetid: fc39d63b-a210-4760-9027-eb315f63924d
ms.date: 12/05/2018
ms.keywords: ObjectContext interface [COM+],get_Item method, ObjectContext.get_Item, ObjectContext::get_Item, _cos_ObjectContext_get_Item, comsvcs/ObjectContext::get_Item, cos.objectcontext_get_item, get_Item, get_Item method [COM+], get_Item method [COM+],ObjectContext interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ObjectContext::get_Item
 - comsvcs/ObjectContext::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ObjectContext.get_Item
---

# ObjectContext::get_Item


## -description

Retrieves a named property.

## -parameters

### -param name [in]

The name of the property to be retrieved.

### -param pItem [out]

A reference to the retrieved property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>