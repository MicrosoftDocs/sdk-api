---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

