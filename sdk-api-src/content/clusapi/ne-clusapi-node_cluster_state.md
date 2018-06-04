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
 

 

