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

# CLUSTER_NODE_ENUM enumeration


## -description


Describes the types of cluster objects that are enumerated by the 
    <a href="https://msdn.microsoft.com/e184ef8e-9ec6-4d84-a3d0-850298262b81">ClusterNodeEnum</a> and 
    <a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a> functions.


## -enum-fields




### -field CLUSTER_NODE_ENUM_NETINTERFACES

Network interfaces on the node.


#### - CLUSTER_NODE_ENUM_GROUPS

Cluster groups on the node.

<b>Windows Server 2008:  </b>This value is not supported before 
        Windows Server 2008 R2.


#### - CLUSTER_NODE_ENUM_PREFERRED_GROUPS

Cluster groups that list this node as their preferred owner.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is supported before 
        Windows Server 2012 R2.


### -field CLUSTER_NODE_ENUM_ALL

Network interfaces on the node, groups on the node, and groups that list the node as their preferred owner..


## -see-also




<a href="https://msdn.microsoft.com/e184ef8e-9ec6-4d84-a3d0-850298262b81">ClusterNodeEnum</a>



<a href="https://msdn.microsoft.com/f187f4d7-24c8-477d-91fc-0ef738b66f22">ClusterNodeOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

