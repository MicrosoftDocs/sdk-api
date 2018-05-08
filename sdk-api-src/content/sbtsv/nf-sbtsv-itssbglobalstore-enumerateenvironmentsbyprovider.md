---
UID: NF:sbtsv.ITsSbGlobalStore.EnumerateEnvironmentsByProvider
title: ITsSbGlobalStore::EnumerateEnvironmentsByProvider
author: windows-driver-content
description: Returns an array that contains the environments present on the specified provider.
old-location: termserv\itssbglobalstore_enumerateenvironmentsbyprovider.htm
old-project: TermServ
ms.assetid: 4fb29524-61e3-4d1a-be98-45f61b796e9e
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: EnumerateEnvironmentsByProvider, EnumerateEnvironmentsByProvider method [Remote Desktop Services], EnumerateEnvironmentsByProvider method [Remote Desktop Services],ITsSbGlobalStore interface, ITsSbGlobalStore interface [Remote Desktop Services],EnumerateEnvironmentsByProvider method, ITsSbGlobalStore.EnumerateEnvironmentsByProvider, ITsSbGlobalStore::EnumerateEnvironmentsByProvider, sbtsv/ITsSbGlobalStore::EnumerateEnvironmentsByProvider, termserv.itssbglobalstore_enumerateenvironmentsbyprovider
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
-	ITsSbGlobalStore.EnumerateEnvironmentsByProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITsSbGlobalStore::EnumerateEnvironmentsByProvider


## -description


Returns an array that contains the environments present on the specified provider.


## -parameters




### -param ProviderName [in]

The name of the provider.


### -param pdwCount [in, out]

A pointer to the number of environments retrieved.


### -param ppVal [out]

A pointer to an array that contains references to the environments present. When you have finished using the array, release each element and free the array by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d25b6f73-ee5f-40e4-9c49-fd48dd3990d2">ITsSbGlobalStore</a>
 

 

