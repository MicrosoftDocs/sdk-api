---
UID: NF:msclus.ISClusNode.get_State
title: ISClusNode::get_State
author: windows-sdk-content
description: State of a node.
old-location: mscs\clusnode_state.htm
old-project: mscs
ms.assetid: c1887055-518a-4177-a618-418c75883d69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNode object [Failover Cluster],State property, ClusNode.State, ClusterNodeDown, ClusterNodeJoining, ClusterNodePaused, ClusterNodeStateUnknown, ClusterNodeUp, ISClusNode.get_State, ISClusNode::get_State, State property [Failover Cluster], State property [Failover Cluster],ClusNode object, _wolf_clusnode.state, get_State, mscs.clusnode_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusNode.State
 - ISClusNode.get_State
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::get_State


## -description


<p class="CCE_Message">[The <b>State</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Retrieves the state of a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



The <b>ClusterNodeDown</b> state only indicates that a node is inactive; it does not 
    specify the reason for the inactivity. A node can be in the <b>ClusterNodeDown</b> state for 
    the following reasons:

<ul>
<li>The node is not running.</li>
<li>The <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> on the node is not 
      running.</li>
<li>The node cannot communicate with the node controlling the 
      <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.</li>
<li>The node is inactive for any other reason.</li>
</ul>
When a node is operating as an active member of a cluster but cannot host any resources or groups, it is in 
    the <b>ClusterNodePaused</b> state (see the 
    <a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a> function). Nodes that are undergoing 
    maintenance are typically placed in this state.

For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/25bc275e-8d9c-43b3-8f95-dd3fd2cbe3ce">CLUSTER_NODE_STATE</a>



<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>
 

 

