---
UID: NF:propsys.IPropertyStoreCache.GetState
title: IPropertyStoreCache::GetState method
author: windows-driver-content
description: Gets the state of a specified property key.
old-location: properties\IPropertyStoreCache_GetState.htm
old-project: properties
ms.assetid: bee9275d-9529-4285-8dee-8e4683def46d
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetState method [Windows Properties], GetState method [Windows Properties], IPropertyStoreCache interface, GetState,IPropertyStoreCache.GetState, IPropertyStoreCache, IPropertyStoreCache interface [Windows Properties], GetState method, IPropertyStoreCache::GetState, _shell_IPropertyStoreCache_GetState, properties.IPropertyStoreCache_GetState, propsys/IPropertyStoreCache::GetState, shell.IPropertyStoreCache_GetState
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyStoreCache.GetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyStoreCache::GetState method


## -description


Gets the state of a specified property key.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure.


### -param pstate [out]

Type: <b><a href="shell.PSC_STATE">PSC_STATE</a>*</b>

A pointer to a <a href="shell.PSC_STATE">PSC_STATE</a> enumeration value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



