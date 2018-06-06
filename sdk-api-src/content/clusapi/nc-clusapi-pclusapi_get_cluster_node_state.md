---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_NODE_STATE
title: PCLUSAPI_GET_CLUSTER_NODE_STATE
author: windows-sdk-content
description: Returns the current state of a node.
old-location: mscs\getclusternodestate.htm
old-project: MsCS
ms.assetid: 94c83582-3d99-4a20-ad58-1af4e8190781
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_NODE_STATE, PCLUSAPI_GET_CLUSTER_NODE_STATE callback, PCLUSAPI_GET_CLUSTER_NODE_STATE callback function [Failover Cluster], _wolf_getclusternodestate, clusapi/PCLUSAPI_GET_CLUSTER_NODE_STATE, mscs.getclusternodestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_GET_CLUSTER_NODE_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_NODE_STATE callback function


## -description


Returns the 
    current state of a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>. The <b>PCLUSAPI_GET_CLUSTER_NODE_STATE</b> type defines a pointer to this function.


## -parameters




### -param hNode [in]

Handle to the node for which state information should be returned.


## -returns



<i>GetClusterNodeState</i> returns the current state 
       of the node, which is represented by one of the following values.


The returned values are from the 
       <a href="https://msdn.microsoft.com/25bc275e-8d9c-43b3-8f95-dd3fd2cbe3ce">CLUSTER_NODE_STATE</a> enumeration.






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




## -see-also




<a href="https://msdn.microsoft.com/25bc275e-8d9c-43b3-8f95-dd3fd2cbe3ce">CLUSTER_NODE_STATE</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/23b4ff74-f72f-4227-9b69-ff36fa6ed55b">PauseClusterNode</a>
 

 

