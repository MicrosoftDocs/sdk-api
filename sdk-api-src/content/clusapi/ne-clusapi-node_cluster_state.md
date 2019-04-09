---
UID: NE:clusapi.NODE_CLUSTER_STATE
title: NODE_CLUSTER_STATE (clusapi.h)
author: windows-sdk-content
description: Indicates the state of the cluster.
old-location: mscs\node_cluster_state.htm
tech.root: MsCS
ms.assetid: cc3b5bdc-79d7-4578-bfa5-8e57df4670e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CLUSTER_CONFIGURED, CLUSTER_INSTALLED, CLUSTER_RUNNING, ClusterStateNotConfigured, ClusterStateNotInstalled, ClusterStateNotRunning, ClusterStateRunning, NODE_CLUSTER_STATE, NODE_CLUSTER_STATE enumeration [Failover Cluster], _NODE_CLUSTER_STATE, _NODE_CLUSTER_STATE enumeration [Failover Cluster], clusapi/ClusterStateNotConfigured, clusapi/ClusterStateNotInstalled, clusapi/ClusterStateNotRunning, clusapi/ClusterStateRunning, clusapi/NODE_CLUSTER_STATE, clusapi/_NODE_CLUSTER_STATE, msclus/ClusterStateNotConfigured, msclus/ClusterStateNotInstalled, msclus/ClusterStateNotRunning, msclus/ClusterStateRunning, msclus/NODE_CLUSTER_STATE, msclus/_NODE_CLUSTER_STATE, mscs.node_cluster_state
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - NODE_CLUSTER_STATE
product: Windows
targetos: Windows
req.typenames: NODE_CLUSTER_STATE
req.redist: 
---

# NODE_CLUSTER_STATE enumeration


## -description


Indicates the state of the cluster. The 
     <a href="https://msdn.microsoft.com/67534bc8-f19e-4330-850a-788a7f031f5b">GetNodeClusterState</a> function uses this 
     enumeration.


## -enum-fields




### -field ClusterStateNotInstalled

The Cluster service is not installed on the node.


### -field ClusterStateNotConfigured

The Cluster service is installed on the node but has not yet been configured.


### -field ClusterStateNotRunning

The Cluster service is installed and configured on the node but is not currently running.


### -field ClusterStateRunning

The Cluster service is installed, configured, and running on the node.


## -remarks



The following constants are defined in ClusAPI.h.

<table>
<tr>
<th>Constant</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>CLUSTER_INSTALLED</b>

</td>
<td>
0x00000001

</td>
</tr>
<tr>
<td>
<b>CLUSTER_CONFIGURED</b>

</td>
<td>
0x00000002

</td>
</tr>
<tr>
<td>
<b>CLUSTER_RUNNING</b>

</td>
<td>
0x00000010

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/67534bc8-f19e-4330-850a-788a7f031f5b">GetNodeClusterState</a>
 

 

