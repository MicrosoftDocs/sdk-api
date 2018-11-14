---
UID: NE:clusapi.CLUSTER_ENUM
title: CLUSTER_ENUM
author: windows-sdk-content
description: Describes the type of cluster objects being enumerated.
old-location: mscs\cluster_enum.htm
tech.root: mscs
ms.assetid: e3d5a207-d30e-4935-be95-0957e68d4fe6
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CLUSTER_ENUM, CLUSTER_ENUM enumeration [Failover Cluster], CLUSTER_ENUM_ALL, CLUSTER_ENUM_GROUP, CLUSTER_ENUM_INTERNAL_NETWORK, CLUSTER_ENUM_NETINTERFACE, CLUSTER_ENUM_NETWORK, CLUSTER_ENUM_NODE, CLUSTER_ENUM_RESOURCE, CLUSTER_ENUM_RESTYPE, CLUSTER_ENUM_SHARED_VOLUME_GROUP, CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, _CLUSTER_ENUM, _CLUSTER_ENUM enumeration [Failover Cluster], clusapi/CLUSTER_ENUM, clusapi/CLUSTER_ENUM_ALL, clusapi/CLUSTER_ENUM_GROUP, clusapi/CLUSTER_ENUM_INTERNAL_NETWORK, clusapi/CLUSTER_ENUM_NETINTERFACE, clusapi/CLUSTER_ENUM_NETWORK, clusapi/CLUSTER_ENUM_NODE, clusapi/CLUSTER_ENUM_RESOURCE, clusapi/CLUSTER_ENUM_RESTYPE, clusapi/CLUSTER_ENUM_SHARED_VOLUME_GROUP, clusapi/CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, clusapi/_CLUSTER_ENUM, msclus/CLUSTER_ENUM, msclus/CLUSTER_ENUM_ALL, msclus/CLUSTER_ENUM_GROUP, msclus/CLUSTER_ENUM_INTERNAL_NETWORK, msclus/CLUSTER_ENUM_NETINTERFACE, msclus/CLUSTER_ENUM_NETWORK, msclus/CLUSTER_ENUM_NODE, msclus/CLUSTER_ENUM_RESOURCE, msclus/CLUSTER_ENUM_RESTYPE, msclus/CLUSTER_ENUM_SHARED_VOLUME_GROUP, msclus/CLUSTER_ENUM_SHARED_VOLUME_RESOURCE, msclus/_CLUSTER_ENUM, mscs.cluster_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CLUSTER_ENUM
product: Windows
targetos: Windows
req.typenames: CLUSTER_ENUM
req.redist: 
---

# CLUSTER_ENUM enumeration


## -description


Describes the type of cluster objects being enumerated. This enumeration is used by the 
    <a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a> and 
    <a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a> functions.


## -enum-fields




### -field CLUSTER_ENUM_NODE

The <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> in the cluster.


### -field CLUSTER_ENUM_RESTYPE

The <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> in the cluster.


### -field CLUSTER_ENUM_RESOURCE

The <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in the cluster.


### -field CLUSTER_ENUM_GROUP

The <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> in the cluster.


### -field CLUSTER_ENUM_NETWORK

The <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> in the cluster.


### -field CLUSTER_ENUM_NETINTERFACE

The <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> in the cluster.


### -field CLUSTER_ENUM_SHARED_VOLUME_GROUP

The cluster shared volumes (CSV) in the cluster.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not supported before 
        Windows Server 2012 R2.


### -field CLUSTER_ENUM_SHARED_VOLUME_RESOURCE

The cluster shared volumes in the cluster.

<b>Windows Server 2008:  </b>This value is not supported before 
        Windows Server 2008 R2.


### -field CLUSTER_ENUM_INTERNAL_NETWORK

The networks used by the cluster for internal communication.


### -field CLUSTER_ENUM_ALL

All the cluster objects.


## -see-also




<a href="https://msdn.microsoft.com/a7511ac6-04cb-407b-90aa-3382c5160cb6">ClusterEnum</a>



<a href="https://msdn.microsoft.com/b6eb5c03-dd6e-42ef-a020-cf0d61143040">ClusterOpenEnum</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

