---
UID: NF:sbtsv.ITsSbGlobalStore.GetFarmProperty
title: ITsSbGlobalStore::GetFarmProperty (sbtsv.h)
description: Retrieves a property of a farm.helpviewer_keywords: ["GetFarmProperty","GetFarmProperty method [Remote Desktop Services]","GetFarmProperty method [Remote Desktop Services]","ITsSbGlobalStore interface","ITsSbGlobalStore interface [Remote Desktop Services]","GetFarmProperty method","ITsSbGlobalStore.GetFarmProperty","ITsSbGlobalStore::GetFarmProperty","sbtsv/ITsSbGlobalStore::GetFarmProperty","termserv.itssbglobalstore_getfarmproperty"]
old-location: termserv\itssbglobalstore_getfarmproperty.htm
tech.root: TermServ
ms.assetid: 14b9ca43-735d-43d1-bda5-d84cc9a7761a
ms.date: 12/05/2018
ms.keywords: GetFarmProperty, GetFarmProperty method [Remote Desktop Services], GetFarmProperty method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],GetFarmProperty method, ITsSbGlobalStore.GetFarmProperty, ITsSbGlobalStore::GetFarmProperty, sbtsv/ITsSbGlobalStore::GetFarmProperty, termserv.itssbglobalstore_getfarmproperty
f1_keywords:
- sbtsv/ITsSbGlobalStore.GetFarmProperty
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sbtsv.h
api_name:
- ITsSbGlobalStore.GetFarmProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbGlobalStore::GetFarmProperty


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>
 

 

