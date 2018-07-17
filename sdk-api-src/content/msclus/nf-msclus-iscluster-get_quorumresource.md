---
UID: NF:msclus.ISCluster.get_QuorumResource
title: ISCluster::get_QuorumResource
author: windows-sdk-content
description: Returns the current quorum resource for a cluster or allows a new quorum resource to be designated.
old-location: mscs\cluster_quorumresource.htm
old-project: mscs
ms.assetid: e9c1f32a-2008-470e-b451-312cce49c93a
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: Cluster object [Failover Cluster],QuorumResource property, Cluster.QuorumResource, ISCluster.get_QuorumResource, ISCluster.put_QuorumResource, ISCluster::get_QuorumResource, QuorumResource property [Failover Cluster], QuorumResource property [Failover Cluster],Cluster object, _wolf_cluster.quorumresource, get_QuorumResource, mscs.cluster_quorumresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - Cluster.QuorumResource
 - ISCluster.get_QuorumResource
 - ISCluster.put_QuorumResource
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISCluster::get_QuorumResource


## -description


<p class="CCE_Message">[The <b>QuorumResource</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    current <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> for a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> or allows a new quorum resource to be 
    designated.

This property is read/write.


## -parameters


## -remarks



An alternate way to assign a quorum resource is to call that resource's 
    <a href="https://msdn.microsoft.com/fd316586-8553-4c4a-824e-ee5b7bf48184">ClusResource.BecomeQuorumResource</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/fd316586-8553-4c4a-824e-ee5b7bf48184">ClusResource.BecomeQuorumResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

