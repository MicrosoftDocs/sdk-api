---
UID: NF:sbtsv.ITsSbGlobalStore.GetFarmProperty
title: ITsSbGlobalStore::GetFarmProperty
author: windows-driver-content
description: Retrieves a property of a farm.
old-location: termserv\itssbglobalstore_getfarmproperty.htm
old-project: TermServ
ms.assetid: 14b9ca43-735d-43d1-bda5-d84cc9a7761a
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetFarmProperty, GetFarmProperty method [Remote Desktop Services], GetFarmProperty method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],GetFarmProperty method, ITsSbGlobalStore.GetFarmProperty, ITsSbGlobalStore::GetFarmProperty, sbtsv/ITsSbGlobalStore::GetFarmProperty, termserv.itssbglobalstore_getfarmproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbGlobalStore.GetFarmProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

