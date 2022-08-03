---
UID: NS:clusapi._CLUSTER_ENUM_ITEM
title: CLUSTER_ENUM_ITEM (clusapi.h)
description: CLUSTER_ENUM_ITEM contains the properties of a cluster object and is used to enumerate clusters in the ClusterEnumEx and ClusterNodeEnumEx functions.
helpviewer_keywords: ["*PCLUSTER_ENUM_ITEM","CLUSTER_ENUM_ITEM","CLUSTER_ENUM_ITEM structure [Failover Cluster]","PCLUSTER_ENUM_ITEM","PCLUSTER_ENUM_ITEM structure pointer [Failover Cluster]","_CLUSTER_ENUM_ITEM","_CLUSTER_ENUM_ITEM structure [Failover Cluster]","clusapi/CLUSTER_ENUM_ITEM","clusapi/PCLUSTER_ENUM_ITEM","clusapi/_CLUSTER_ENUM_ITEM","msclus/CLUSTER_ENUM_ITEM","msclus/PCLUSTER_ENUM_ITEM","msclus/_CLUSTER_ENUM_ITEM","mscs.cluster_enum_item"]
old-location: mscs\cluster_enum_item.htm
tech.root: MsCS
ms.assetid: 2E7FB4DA-88AD-4739-ACE0-D43670F914D4
ms.date: 08/03/2022
ms.keywords: '*PCLUSTER_ENUM_ITEM, CLUSTER_ENUM_ITEM, CLUSTER_ENUM_ITEM structure [Failover Cluster], PCLUSTER_ENUM_ITEM, PCLUSTER_ENUM_ITEM structure pointer [Failover Cluster], _CLUSTER_ENUM_ITEM, _CLUSTER_ENUM_ITEM structure [Failover Cluster], clusapi/CLUSTER_ENUM_ITEM, clusapi/PCLUSTER_ENUM_ITEM, clusapi/_CLUSTER_ENUM_ITEM, msclus/CLUSTER_ENUM_ITEM, msclus/PCLUSTER_ENUM_ITEM, msclus/_CLUSTER_ENUM_ITEM, mscs.cluster_enum_item'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: CLUSTER_ENUM_ITEM, *PCLUSTER_ENUM_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_ENUM_ITEM
 - clusapi/_CLUSTER_ENUM_ITEM
 - PCLUSTER_ENUM_ITEM
 - clusapi/PCLUSTER_ENUM_ITEM
 - CLUSTER_ENUM_ITEM
 - clusapi/CLUSTER_ENUM_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MSClus.h
api_name:
 - CLUSTER_ENUM_ITEM
---

# CLUSTER_ENUM_ITEM structure


## -description

Contains the properties of a cluster object. This structure is used to enumerate clusters in the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterenumex">ClusterEnumEx</a> and <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeenumex">ClusterNodeEnumEx</a> functions.

## -struct-fields

### -field dwVersion

The version of the <b>CLUSTER_ENUM_ITEM</b> structure.

### -field dwType

A bitmask that specifies the type of the cluster object.

### -field cbId

The size, in bytes, of the <b>lpszId</b> field.

### -field lpszId

The ID of the cluster.

### -field cbName

The size, in bytes, of the <b>lpszName</b> field.

### -field lpszName

The name of the cluster.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterenumex">ClusterEnumEx</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternodeenumex">ClusterNodeEnumEx</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>
