---
UID: NF:sbtsv.ITsSbResourcePluginStore.EnumerateEnvironments
title: ITsSbResourcePluginStore::EnumerateEnvironments method
author: windows-driver-content
description: Returns an array that contains the environments present in the resource plug-in store.
old-location: termserv\itssbresourcepluginstore_enumerateenvironments.htm
old-project: TermServ
ms.assetid: 5c9d2fb4-05e7-449d-8326-b983701b3302
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumerateEnvironments method [Remote Desktop Services], EnumerateEnvironments method [Remote Desktop Services], ITsSbResourcePluginStore interface, EnumerateEnvironments method [Remote Desktop Services], ITsSbResourcePluginStoreEx interface, EnumerateEnvironments,ITsSbResourcePluginStore.EnumerateEnvironments, ITsSbResourcePluginStore, ITsSbResourcePluginStore interface [Remote Desktop Services], EnumerateEnvironments method, ITsSbResourcePluginStore::EnumerateEnvironments, ITsSbResourcePluginStoreEx interface [Remote Desktop Services], EnumerateEnvironments method, ITsSbResourcePluginStoreEx::EnumerateEnvironments, sbtsv/ITsSbResourcePluginStore::EnumerateEnvironments, sbtsv/ITsSbResourcePluginStoreEx::EnumerateEnvironments, termserv.itssbresourcepluginstore_enumerateenvironments
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
-	ITsSbResourcePluginStore.EnumerateEnvironments
-	ITsSbResourcePluginStoreEx.EnumerateEnvironments
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbResourcePluginStore::EnumerateEnvironments method


## -description


Returns an array that contains the environments present in the resource plug-in store.


## -parameters




### -param pdwCount [in, out]

A pointer to the number of targets retrieved.


### -param pVal [out]

A pointer to an array that contains references to the environments present. When you have finished using the array, release each element and free the array by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/287cea18-c13c-4396-8970-39dd7f9b960e">ITsSbEnvironment</a>



<a href="https://msdn.microsoft.com/b8b54827-6c6b-4531-8ae3-73baed6125cd">ITsSbResourcePluginStore</a>



<a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a>
 

 

