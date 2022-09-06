---
UID: NE:clusapi.CLUSTER_OBJECT_TYPE
title: CLUSTER_OBJECT_TYPE (clusapi.h)
description: Defines the type of object for which a notification is requested or generated.
helpviewer_keywords: ["CLUSTER_OBJECT_TYPE","CLUSTER_OBJECT_TYPE enumeration [Failover Cluster]","CLUSTER_OBJECT_TYPE_CLUSTER","CLUSTER_OBJECT_TYPE_GROUP","CLUSTER_OBJECT_TYPE_GROUPSET","CLUSTER_OBJECT_TYPE_NETWORK","CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE","CLUSTER_OBJECT_TYPE_NODE","CLUSTER_OBJECT_TYPE_NONE","CLUSTER_OBJECT_TYPE_QUORUM","CLUSTER_OBJECT_TYPE_REGISTRY","CLUSTER_OBJECT_TYPE_RESOURCE","CLUSTER_OBJECT_TYPE_RESOURCE_TYPE","CLUSTER_OBJECT_TYPE_SHARED_VOLUME","clusapi/CLUSTER_OBJECT_TYPE","clusapi/CLUSTER_OBJECT_TYPE_CLUSTER","clusapi/CLUSTER_OBJECT_TYPE_GROUP","clusapi/CLUSTER_OBJECT_TYPE_GROUPSET","clusapi/CLUSTER_OBJECT_TYPE_NETWORK","clusapi/CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE","clusapi/CLUSTER_OBJECT_TYPE_NODE","clusapi/CLUSTER_OBJECT_TYPE_NONE","clusapi/CLUSTER_OBJECT_TYPE_QUORUM","clusapi/CLUSTER_OBJECT_TYPE_REGISTRY","clusapi/CLUSTER_OBJECT_TYPE_RESOURCE","clusapi/CLUSTER_OBJECT_TYPE_RESOURCE_TYPE","clusapi/CLUSTER_OBJECT_TYPE_SHARED_VOLUME","msclus/CLUSTER_OBJECT_TYPE","msclus/CLUSTER_OBJECT_TYPE_CLUSTER","msclus/CLUSTER_OBJECT_TYPE_GROUP","msclus/CLUSTER_OBJECT_TYPE_GROUPSET","msclus/CLUSTER_OBJECT_TYPE_NETWORK","msclus/CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE","msclus/CLUSTER_OBJECT_TYPE_NODE","msclus/CLUSTER_OBJECT_TYPE_NONE","msclus/CLUSTER_OBJECT_TYPE_QUORUM","msclus/CLUSTER_OBJECT_TYPE_REGISTRY","msclus/CLUSTER_OBJECT_TYPE_RESOURCE","msclus/CLUSTER_OBJECT_TYPE_RESOURCE_TYPE","msclus/CLUSTER_OBJECT_TYPE_SHARED_VOLUME","mscs.cluster_object_type"]
old-location: mscs\cluster_object_type.htm
tech.root: MsCS
ms.assetid: 714C0EF1-7397-4227-B4B1-AFC5E61E08C2
ms.date: 12/05/2018
ms.keywords: CLUSTER_OBJECT_TYPE, CLUSTER_OBJECT_TYPE enumeration [Failover Cluster], CLUSTER_OBJECT_TYPE_CLUSTER, CLUSTER_OBJECT_TYPE_GROUP, CLUSTER_OBJECT_TYPE_GROUPSET, CLUSTER_OBJECT_TYPE_NETWORK, CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE, CLUSTER_OBJECT_TYPE_NODE, CLUSTER_OBJECT_TYPE_NONE, CLUSTER_OBJECT_TYPE_QUORUM, CLUSTER_OBJECT_TYPE_REGISTRY, CLUSTER_OBJECT_TYPE_RESOURCE, CLUSTER_OBJECT_TYPE_RESOURCE_TYPE, CLUSTER_OBJECT_TYPE_SHARED_VOLUME, clusapi/CLUSTER_OBJECT_TYPE, clusapi/CLUSTER_OBJECT_TYPE_CLUSTER, clusapi/CLUSTER_OBJECT_TYPE_GROUP, clusapi/CLUSTER_OBJECT_TYPE_GROUPSET, clusapi/CLUSTER_OBJECT_TYPE_NETWORK, clusapi/CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE, clusapi/CLUSTER_OBJECT_TYPE_NODE, clusapi/CLUSTER_OBJECT_TYPE_NONE, clusapi/CLUSTER_OBJECT_TYPE_QUORUM, clusapi/CLUSTER_OBJECT_TYPE_REGISTRY, clusapi/CLUSTER_OBJECT_TYPE_RESOURCE, clusapi/CLUSTER_OBJECT_TYPE_RESOURCE_TYPE, clusapi/CLUSTER_OBJECT_TYPE_SHARED_VOLUME, msclus/CLUSTER_OBJECT_TYPE, msclus/CLUSTER_OBJECT_TYPE_CLUSTER, msclus/CLUSTER_OBJECT_TYPE_GROUP, msclus/CLUSTER_OBJECT_TYPE_GROUPSET, msclus/CLUSTER_OBJECT_TYPE_NETWORK, msclus/CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE, msclus/CLUSTER_OBJECT_TYPE_NODE, msclus/CLUSTER_OBJECT_TYPE_NONE, msclus/CLUSTER_OBJECT_TYPE_QUORUM, msclus/CLUSTER_OBJECT_TYPE_REGISTRY, msclus/CLUSTER_OBJECT_TYPE_RESOURCE, msclus/CLUSTER_OBJECT_TYPE_RESOURCE_TYPE, msclus/CLUSTER_OBJECT_TYPE_SHARED_VOLUME, mscs.cluster_object_type
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
targetos: Windows
req.typenames: CLUSTER_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_OBJECT_TYPE
 - clusapi/CLUSTER_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUSTER_OBJECT_TYPE
---

# CLUSTER_OBJECT_TYPE enumeration


## -description

Defines the type of object for which a notification is requested or generated.

## -enum-fields

### -field CLUSTER_OBJECT_TYPE_NONE:0x00000000

The notification is for an unspecified type.

### -field CLUSTER_OBJECT_TYPE_CLUSTER:0x00000001

The notification is for the cluster.

### -field CLUSTER_OBJECT_TYPE_GROUP:0x00000002

The notification is for a group.

### -field CLUSTER_OBJECT_TYPE_RESOURCE:0x00000003

The notification is for a resource.

### -field CLUSTER_OBJECT_TYPE_RESOURCE_TYPE:0x00000004

The notification is for a resource type.

### -field CLUSTER_OBJECT_TYPE_NETWORK_INTERFACE:0x00000005

The notification is for a cluster network interface.

### -field CLUSTER_OBJECT_TYPE_NETWORK:0x00000006

The notification is for a cluster network.

### -field CLUSTER_OBJECT_TYPE_NODE:0x00000007

The notification is for a cluster node.

### -field CLUSTER_OBJECT_TYPE_REGISTRY:0x00000008

The notification is for a cluster registry key.

### -field CLUSTER_OBJECT_TYPE_QUORUM:0x00000009

The notification is for a quorum resource.

### -field CLUSTER_OBJECT_TYPE_SHARED_VOLUME:0x0000000a

The notification is for a cluster shared volume.

### -field CLUSTER_OBJECT_TYPE_GROUPSET:0x0000000d

The notification is for a groupset.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is unavailable prior to Windows Server 2016.

