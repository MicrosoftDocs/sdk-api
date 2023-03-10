---
UID: NF:sbtsv.ITsSbResourcePluginStore.GetFarmProperty
title: ITsSbResourcePluginStore::GetFarmProperty (sbtsv.h)
description: Retrieves a property of a farm. (ITsSbResourcePluginStoreEx.GetFarmProperty)
helpviewer_keywords: ["GetFarmProperty","GetFarmProperty method [Remote Desktop Services]","GetFarmProperty method [Remote Desktop Services]","ITsSbResourcePluginStore interface","GetFarmProperty method [Remote Desktop Services]","ITsSbResourcePluginStoreEx interface","ITsSbResourcePluginStore interface [Remote Desktop Services]","GetFarmProperty method","ITsSbResourcePluginStore.GetFarmProperty","ITsSbResourcePluginStore::GetFarmProperty","ITsSbResourcePluginStoreEx interface [Remote Desktop Services]","GetFarmProperty method","ITsSbResourcePluginStoreEx::GetFarmProperty","sbtsv/ITsSbResourcePluginStore::GetFarmProperty","sbtsv/ITsSbResourcePluginStoreEx::GetFarmProperty","termserv.itssbresourcepluginstore_getfarmproperty"]
old-location: termserv\itssbresourcepluginstore_getfarmproperty.htm
tech.root: TermServ
ms.assetid: 83cf8f54-99c2-46fb-b882-e2f3c31240e9
ms.date: 12/05/2018
ms.keywords: GetFarmProperty, GetFarmProperty method [Remote Desktop Services], GetFarmProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, GetFarmProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],GetFarmProperty method, ITsSbResourcePluginStore.GetFarmProperty, ITsSbResourcePluginStore::GetFarmProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],GetFarmProperty method, ITsSbResourcePluginStoreEx::GetFarmProperty, sbtsv/ITsSbResourcePluginStore::GetFarmProperty, sbtsv/ITsSbResourcePluginStoreEx::GetFarmProperty, termserv.itssbresourcepluginstore_getfarmproperty
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbResourcePluginStore::GetFarmProperty
 - sbtsv/ITsSbResourcePluginStore::GetFarmProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore.GetFarmProperty
 - ITsSbResourcePluginStoreEx.GetFarmProperty
---

# ITsSbResourcePluginStore::GetFarmProperty


## -description

Retrieves a property of a farm.

## -parameters

### -param farmName [in]

The name of the farm.

### -param propertyName [in]

The name of the property to retrieve.

### -param pVarValue [in]

Returns a pointer to the value of the property.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore">ITsSbResourcePluginStore</a>



<a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a>
