---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateTargets
title: ITsSbGlobalStore::EnumerateTargets
author: windows-driver-content
description: Returns an array that contains the specified targets present in the global store.
old-location: termserv\itssbglobalstore_enumeratetargets.htm
old-project: TermServ
ms.assetid: 939d967f-6846-4ef2-9943-a171eac6cb21
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EnumerateTargets, EnumerateTargets method [Remote Desktop Services], EnumerateTargets method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateTargets method, ITsSbGlobalStore.EnumerateTargets, ITsSbGlobalStore::EnumerateTargets, sbtsv/ITsSbGlobalStore::EnumerateTargets, termserv.itssbglobalstore_enumeratetargets
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
-	ITsSbGlobalStore.EnumerateTargets
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbGlobalStore::EnumerateTargets


## -description


Returns an array that contains the specified targets present in the global store. 


## -parameters




### -param ProviderName [in]

The provider name.


### -param FarmName [in]

The farm name.


### -param EnvName [in]

The environment name.


### -param pdwCount [in, out]

The number of targets retrieved.


### -param pVal [out]

Pointer to the retrieved <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>
     objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

