---
UID: NF:propsys.IPropertyStoreCache.GetValueAndState
title: IPropertyStoreCache::GetValueAndState (propsys.h)
description: Gets value and state data for a property key.
helpviewer_keywords: ["GetValueAndState","GetValueAndState method [Windows Properties]","GetValueAndState method [Windows Properties]","IPropertyStoreCache interface","IPropertyStoreCache interface [Windows Properties]","GetValueAndState method","IPropertyStoreCache.GetValueAndState","IPropertyStoreCache::GetValueAndState","properties.IPropertyStoreCache_GetValueAndState","propsys/IPropertyStoreCache::GetValueAndState","shell.IPropertyStoreCache_GetValueAndState","shell_IPropertyStoreCache_GetValueAndState"]
old-location: properties\IPropertyStoreCache_GetValueAndState.htm
tech.root: properties
ms.assetid: eb8866c9-fc14-42c0-aaed-bd192ca25cf6
ms.date: 12/05/2018
ms.keywords: GetValueAndState, GetValueAndState method [Windows Properties], GetValueAndState method [Windows Properties],IPropertyStoreCache interface, IPropertyStoreCache interface [Windows Properties],GetValueAndState method, IPropertyStoreCache.GetValueAndState, IPropertyStoreCache::GetValueAndState, properties.IPropertyStoreCache_GetValueAndState, propsys/IPropertyStoreCache::GetValueAndState, shell.IPropertyStoreCache_GetValueAndState, shell_IPropertyStoreCache_GetValueAndState
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
 - IPropertyStoreCache::GetValueAndState
 - propsys/IPropertyStoreCache::GetValueAndState
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
 - IPropertyStoreCache.GetValueAndState
---

# IPropertyStoreCache::GetValueAndState


## -description

Gets value and state data for a property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure identifying the property.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure for the property data.

### -param pstate [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a>*</b>

A pointer to a <a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a> enumeration value declaring the current state of the property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.