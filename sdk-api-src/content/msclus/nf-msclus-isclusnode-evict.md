---
UID: NF:msclus.ISClusNode.Evict
title: ISClusNode::Evict
author: windows-sdk-content
description: Removes a node from the cluster.
old-location: mscs\clusnode_evict.htm
old-project: mscs
ms.assetid: e65a230e-3931-4e1a-b80d-3fd2499d330c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNode object [Failover Cluster],Evict method, ClusNode.Evict, Evict, Evict method [Failover Cluster], Evict method [Failover Cluster],ClusNode object, ISClusNode.Evict, ISClusNode::Evict, _wolf_clusnode.evict, mscs.clusnode_evict
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
 - ClusNode.Evict
 - ISClusNode.Evict
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::Evict


## -description


<p class="CCE_Message">[The <b>Evict</b> method is available 
    for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Removes a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



An evicted node is no longer a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. 
    The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> must be reinstalled on the node to 
    reestablish the node's cluster membership.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/4a765dce-c823-4a79-8608-ff41feec8a39">Cluster Object</a>
 

 

