---
UID: NF:propsys.IPropertyStoreCache.GetState
title: IPropertyStoreCache::GetState (propsys.h)
author: windows-sdk-content
description: Gets the state of a specified property key.
old-location: properties\IPropertyStoreCache_GetState.htm
tech.root: properties
ms.assetid: bee9275d-9529-4285-8dee-8e4683def46d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Windows Properties], GetState method [Windows Properties],IPropertyStoreCache interface, IPropertyStoreCache interface [Windows Properties],GetState method, IPropertyStoreCache.GetState, IPropertyStoreCache::GetState, _shell_IPropertyStoreCache_GetState, properties.IPropertyStoreCache_GetState, propsys/IPropertyStoreCache::GetState, shell.IPropertyStoreCache_GetState
ms.topic: method
f1_keywords:
- propsys/IPropertyStoreCache.GetState
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Propsys.h
api_name:
- IPropertyStoreCache.GetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStoreCache::GetState


## -description


Gets the state of a specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.


### -param pstate [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-psc_state">PSC_STATE</a> enumeration value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



