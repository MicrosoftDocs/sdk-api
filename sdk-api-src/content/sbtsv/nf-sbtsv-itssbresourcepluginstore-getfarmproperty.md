---
UID: NF:sbtsv.ITsSbResourcePluginStore.GetFarmProperty
title: ITsSbResourcePluginStore::GetFarmProperty
author: windows-driver-content
description: Retrieves a property of a farm.
old-location: termserv\itssbresourcepluginstore_getfarmproperty.htm
old-project: TermServ
ms.assetid: 83cf8f54-99c2-46fb-b882-e2f3c31240e9
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetFarmProperty, GetFarmProperty method [Remote Desktop Services], GetFarmProperty method [Remote Desktop Services],ITsSbResourcePluginStore interface, GetFarmProperty method [Remote Desktop Services],ITsSbResourcePluginStoreEx interface, ITsSbResourcePluginStore interface [Remote Desktop Services],GetFarmProperty method, ITsSbResourcePluginStore.GetFarmProperty, ITsSbResourcePluginStore::GetFarmProperty, ITsSbResourcePluginStoreEx interface [Remote Desktop Services],GetFarmProperty method, ITsSbResourcePluginStoreEx::GetFarmProperty, sbtsv/ITsSbResourcePluginStore::GetFarmProperty, sbtsv/ITsSbResourcePluginStoreEx::GetFarmProperty, termserv.itssbresourcepluginstore_getfarmproperty
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
-	ITsSbResourcePluginStore.GetFarmProperty
-	ITsSbResourcePluginStoreEx.GetFarmProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

