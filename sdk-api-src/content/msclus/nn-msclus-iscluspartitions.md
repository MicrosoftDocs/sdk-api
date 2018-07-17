---
UID: NN:msclus.ISClusPartitions
title: ISClusPartitions
author: windows-sdk-content
description: Provides access to the partitions of a Physical Disk.
old-location: mscs\cluspartitions_collection.htm
old-project: mscs
ms.assetid: 8a3c602a-a3b1-4b63-8dfa-36200c5c30ab
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusPartitions, ClusPartitions collection [Failover Cluster], ClusPartitions collection [Failover Cluster],described, ISClusPartitions, _wolf_cluspartitions_collection, msclus/ClusPartitions, mscs.cluspartitions_collection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusPartitions
 - ISClusPartitions
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusPartitions interface


## -description


<p class="CCE_Message">[The 
    <b>ClusPartitions</b> collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to the partitions of a 
    <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a>.


## -remarks



A <b>ClusPartitions</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/b7af8ab1-83dc-4164-bf59-901cc9fae56f">ClusPartition</a> objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/d0a6ec99-c7c8-4746-aaa7-ee70a2e8f355">ClusDisk.Partitions</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

