---
UID: NN:msclus.ISClusDisks
title: ISClusDisks
author: windows-driver-content
description: Provides access to the cluster-capable Physical Disks available to a resource type.
old-location: mscs\clusdisks_collection.htm
old-project: MsCS
ms.assetid: 2823ccb2-5fb2-4e37-b842-340703165871
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ClusDisks, ClusDisks collection [Failover Cluster], ClusDisks collection [Failover Cluster],described, ISClusDisks, _wolf_clusdisks_collection, msclus/ClusDisks, mscs.clusdisks_collection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusDisks
-	ISClusDisks
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusDisks interface


## -description


<p class="CCE_Message">[The <b>ClusDisks</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]


    Provides access to the 
    <a href="c_gly.htm">cluster-capable</a>
<a href="https://msdn.microsoft.com/003bc879-d526-4f7d-8f58-a9002f78819d">Physical Disks</a> available to a 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>.


## -remarks



A <b>ClusDisks</b> collection contains 
    <a href="https://msdn.microsoft.com/6433d55f-f97a-4027-ba2a-7102b4cf33ae">ClusDisk</a> objects. It is obtained from 
    <a href="https://msdn.microsoft.com/fc700541-793b-423b-bea6-ad04deddb16a">ClusResType.AvailableDisks</a>.




## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

