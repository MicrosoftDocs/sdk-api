---
UID: NF:propsys.IPropertyStoreCache.GetValueAndState
title: IPropertyStoreCache::GetValueAndState
author: windows-sdk-content
description: Gets value and state data for a property key.
old-location: properties\IPropertyStoreCache_GetValueAndState.htm
old-project: properties
ms.assetid: eb8866c9-fc14-42c0-aaed-bd192ca25cf6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetValueAndState, GetValueAndState method [Windows Properties], GetValueAndState method [Windows Properties],IPropertyStoreCache interface, IPropertyStoreCache interface [Windows Properties],GetValueAndState method, IPropertyStoreCache.GetValueAndState, IPropertyStoreCache::GetValueAndState, properties.IPropertyStoreCache_GetValueAndState, propsys/IPropertyStoreCache::GetValueAndState, shell.IPropertyStoreCache_GetValueAndState, shell_IPropertyStoreCache_GetValueAndState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyStoreCache.GetValueAndState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyStoreCache::GetValueAndState


## -description


Gets value and state data for a property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://www.bing.com/search?q=PROPERTYKEY">PROPERTYKEY</a> structure identifying the property.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure for the property data.


### -param pstate [out]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-psc_state.md">PSC_STATE</a>*</b>

A pointer to a <a href="/windows/desktop/api/propsys/ne-propsys-psc_state.md">PSC_STATE</a> enumeration value declaring the current state of the property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



