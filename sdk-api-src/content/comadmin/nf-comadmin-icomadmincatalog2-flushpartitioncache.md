---
UID: NF:comadmin.ICOMAdminCatalog2.FlushPartitionCache
title: ICOMAdminCatalog2::FlushPartitionCache
author: windows-driver-content
description: Empties the cache that maps users to their default partitions.
old-location: cos\icomadmincatalog2_flushpartitioncache.htm
old-project: cossdk
ms.assetid: 8b5f6619-fbff-417d-b80a-a38532227059
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: FlushPartitionCache, FlushPartitionCache method [COM+], FlushPartitionCache method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],FlushPartitionCache method, ICOMAdminCatalog2.FlushPartitionCache, ICOMAdminCatalog2::FlushPartitionCache, _cos_icomadmincatalog2_FlushPartitionCache, comadmin/ICOMAdminCatalog2::FlushPartitionCache, cos.icomadmincatalog2_flushpartitioncache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog2.FlushPartitionCache
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2::FlushPartitionCache


## -description


Empties the cache that maps users to their default partitions.

COM+ caches users' default partitions to avoid repetitive Active Directory requests. You might want to call this method after changing a user's default partition in Active Directory.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

