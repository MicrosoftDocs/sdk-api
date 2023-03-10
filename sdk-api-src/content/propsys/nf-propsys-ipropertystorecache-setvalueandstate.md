---
UID: NF:propsys.IPropertyStoreCache.SetValueAndState
title: IPropertyStoreCache::SetValueAndState (propsys.h)
description: Sets value and state data for a property key.
helpviewer_keywords: ["IPropertyStoreCache interface [Windows Properties]","SetValueAndState method","IPropertyStoreCache.SetValueAndState","IPropertyStoreCache::SetValueAndState","SetValueAndState","SetValueAndState method [Windows Properties]","SetValueAndState method [Windows Properties]","IPropertyStoreCache interface","properties.IPropertyStoreCache_SetValueAndState","propsys/IPropertyStoreCache::SetValueAndState","shell.IPropertyStoreCache_SetValueAndState","shell_IPropertyStoreCache_SetValueAndState"]
old-location: properties\IPropertyStoreCache_SetValueAndState.htm
tech.root: properties
ms.assetid: 2f330b24-339f-420b-871f-6f2ac7bc578c
ms.date: 12/05/2018
ms.keywords: IPropertyStoreCache interface [Windows Properties],SetValueAndState method, IPropertyStoreCache.SetValueAndState, IPropertyStoreCache::SetValueAndState, SetValueAndState, SetValueAndState method [Windows Properties], SetValueAndState method [Windows Properties],IPropertyStoreCache interface, properties.IPropertyStoreCache_SetValueAndState, propsys/IPropertyStoreCache::SetValueAndState, shell.IPropertyStoreCache_SetValueAndState, shell_IPropertyStoreCache_SetValueAndState
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyStoreCache::SetValueAndState
 - propsys/IPropertyStoreCache::SetValueAndState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyStoreCache.SetValueAndState
---

# IPropertyStoreCache::SetValueAndState


## -description

Sets value and state data for a property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure identifying the property.

### -param ppropvar [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure containing the property data.

### -param state [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a></b>

A value from the <a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a> enumeration declaring the state of the property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.