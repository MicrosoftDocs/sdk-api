---
UID: NF:msclus.ISClusNode.Pause
title: ISClusNode::Pause
author: windows-sdk-content
description: Suspends the cluster activity of a node.
old-location: mscs\clusnode_pause.htm
old-project: mscs
ms.assetid: 2fd16dda-b554-47fa-a040-15c7685d6392
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNode object [Failover Cluster],Pause method, ClusNode.Pause, ISClusNode.Pause, ISClusNode::Pause, Pause, Pause method [Failover Cluster], Pause method [Failover Cluster],ClusNode object, _wolf_clusnode.pause, mscs.clusnode_pause
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
 - ClusNode.Pause
 - ISClusNode.Pause
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::Pause


## -description


<p class="CCE_Message">[The <b>Pause</b> method is available 
    for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Suspends the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> activity of a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



Use the <a href="https://msdn.microsoft.com/74e465e2-1328-4e05-b287-3ce27359c67a">ClusNode.Resume</a> method to return a paused 
    node to active status.

While a node is paused, <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> cannot be moved to the node 
    either through the <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a> process or administrator action. A 
    <a href="p_gly.htm">paused</a> node returns 
    <b>ClusterNodePaused</b> as the value for its 
    <a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">ClusNode.State</a> property.

Groups that are owned by a paused node remain owned by that node. A paused node's groups and resources can be 
    taken offline, but they cannot be brought online. Because the paused state is persistent, a paused node continues 
    to be paused when it is rebooted.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/74e465e2-1328-4e05-b287-3ce27359c67a">ClusNode.Resume</a>



<a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">ClusNode.State</a>
 

 

