---
UID: NF:propsys.IPropertyStoreCache.GetState
title: IPropertyStoreCache::GetState (propsys.h)
description: Gets the state of a specified property key.
helpviewer_keywords: ["GetState","GetState method [Windows Properties]","GetState method [Windows Properties]","IPropertyStoreCache interface","IPropertyStoreCache interface [Windows Properties]","GetState method","IPropertyStoreCache.GetState","IPropertyStoreCache::GetState","_shell_IPropertyStoreCache_GetState","properties.IPropertyStoreCache_GetState","propsys/IPropertyStoreCache::GetState","shell.IPropertyStoreCache_GetState"]
old-location: properties\IPropertyStoreCache_GetState.htm
tech.root: properties
ms.assetid: bee9275d-9529-4285-8dee-8e4683def46d
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Properties], GetState method [Windows Properties],IPropertyStoreCache interface, IPropertyStoreCache interface [Windows Properties],GetState method, IPropertyStoreCache.GetState, IPropertyStoreCache::GetState, _shell_IPropertyStoreCache_GetState, properties.IPropertyStoreCache_GetState, propsys/IPropertyStoreCache::GetState, shell.IPropertyStoreCache_GetState
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
 - IPropertyStoreCache::GetState
 - propsys/IPropertyStoreCache::GetState
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
 - IPropertyStoreCache.GetState
---

# IPropertyStoreCache::GetState


## -description

Gets the state of a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pstate [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a>*</b>

A pointer to a <a href="/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a> enumeration value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.