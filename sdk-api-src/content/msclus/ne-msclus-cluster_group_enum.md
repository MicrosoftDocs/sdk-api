---
UID: NE:msclus.CLUSTER_GROUP_ENUM
title: CLUSTER_GROUP_ENUM
author: windows-sdk-content
description: Describes the type of cluster object being enumerated by the ClusterGroupEnum and ClusterGroupOpenEnum functions.
old-location: mscs\cluster_group_enum.htm
tech.root: mscs
ms.assetid: c70bc230-850b-4290-8275-f60ffc8d66bd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CLUSTER_GROUP_ENUM, CLUSTER_GROUP_ENUM enumeration [Failover Cluster], CLUSTER_GROUP_ENUM_ALL, CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, _CLUSTER_GROUP_ENUM, _CLUSTER_GROUP_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_GROUP_ENUM, clusapi/CLUSTER_GROUP_ENUM_ALL, clusapi/CLUSTER_GROUP_ENUM_CONTAINS, clusapi/CLUSTER_GROUP_ENUM_NODES, clusapi/_CLUSTER_GROUP_ENUM, msclus/CLUSTER_GROUP_ENUM, msclus/CLUSTER_GROUP_ENUM_ALL, msclus/CLUSTER_GROUP_ENUM_CONTAINS, msclus/CLUSTER_GROUP_ENUM_NODES, msclus/_CLUSTER_GROUP_ENUM, mscs.cluster_group_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msclus.h
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
 - CLUSTER_GROUP_ENUM
product: Windows
targetos: Windows
req.typenames: CLUSTER_GROUP_ENUM
req.redist: 
---

# CLUSTER_GROUP_ENUM enumeration


## -description


Describes the type of cluster object being enumerated by the 
    <a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a> and 
    <a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a> functions.


## -enum-fields




### -field CLUSTER_GROUP_ENUM_CONTAINS

The resources in the group.


### -field CLUSTER_GROUP_ENUM_NODES

The nodes in the preferred owners list of the group.


### -field CLUSTER_GROUP_ENUM_ALL

All the resources in the group and all the nodes in the preferred owners list of the group.


## -remarks



The <b>CLUSTER_GROUP_ENUM_ALL</b> enumeration value is not a valid value for the 
     <i>lpdwType</i> parameter of the 
     <a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a> function.




## -see-also




<a href="https://msdn.microsoft.com/fffcae88-8df0-487f-9f6d-bc3560283ef1">ClusterGroupEnum</a>



<a href="https://msdn.microsoft.com/d8f9eff0-1784-4b55-8603-c262d5c23f6c">ClusterGroupOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

