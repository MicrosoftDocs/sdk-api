---
UID: NF:propsys.IPropertyStoreCache.SetValueAndState
title: IPropertyStoreCache::SetValueAndState
author: windows-sdk-content
description: Sets value and state data for a property key.
old-location: properties\IPropertyStoreCache_SetValueAndState.htm
tech.root: properties
ms.assetid: 2f330b24-339f-420b-871f-6f2ac7bc578c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPropertyStoreCache interface [Windows Properties],SetValueAndState method, IPropertyStoreCache.SetValueAndState, IPropertyStoreCache::SetValueAndState, SetValueAndState, SetValueAndState method [Windows Properties], SetValueAndState method [Windows Properties],IPropertyStoreCache interface, properties.IPropertyStoreCache_SetValueAndState, propsys/IPropertyStoreCache::SetValueAndState, shell.IPropertyStoreCache_SetValueAndState, shell_IPropertyStoreCache_SetValueAndState
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertyStoreCache.SetValueAndState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStoreCache::SetValueAndState


## -description


Sets value and state data for a property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure identifying the property.


### -param ppropvar [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure containing the property data.


### -param state [in]

Type: <b><a href="shell.PSC_STATE">PSC_STATE</a></b>

A value from the <a href="shell.PSC_STATE">PSC_STATE</a> enumeration declaring the state of the property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



