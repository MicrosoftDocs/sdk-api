---
UID: NE:clusapi.__unnamed_enum_1
title: CLUSTER_MGMT_POINT_TYPE (clusapi.h)
description: Specifies the type of the management point for the cluster.
helpviewer_keywords: ["CLUSTER_MGMT_POINT_TYPE","CLUSTER_MGMT_POINT_TYPE enumeration [Failover Cluster]","CLUSTER_MGMT_POINT_TYPE_CNO","CLUSTER_MGMT_POINT_TYPE_CNO_ONLY","CLUSTER_MGMT_POINT_TYPE_DNS_ONLY","CLUSTER_MGMT_POINT_TYPE_NONE","clusapi/CLUSTER_MGMT_POINT_TYPE","clusapi/CLUSTER_MGMT_POINT_TYPE_CNO","clusapi/CLUSTER_MGMT_POINT_TYPE_CNO_ONLY","clusapi/CLUSTER_MGMT_POINT_TYPE_DNS_ONLY","clusapi/CLUSTER_MGMT_POINT_TYPE_NONE","msclus/CLUSTER_MGMT_POINT_TYPE","msclus/CLUSTER_MGMT_POINT_TYPE_CNO","msclus/CLUSTER_MGMT_POINT_TYPE_CNO_ONLY","msclus/CLUSTER_MGMT_POINT_TYPE_DNS_ONLY","msclus/CLUSTER_MGMT_POINT_TYPE_NONE","mscs.cluster_mgmt_point_type"]
old-location: mscs\cluster_mgmt_point_type.htm
tech.root: MsCS
ms.assetid: 9A849D8E-EC04-470B-A72A-022213CDF92E
ms.date: 12/05/2018
ms.keywords: CLUSTER_MGMT_POINT_TYPE, CLUSTER_MGMT_POINT_TYPE enumeration [Failover Cluster], CLUSTER_MGMT_POINT_TYPE_CNO, CLUSTER_MGMT_POINT_TYPE_CNO_ONLY, CLUSTER_MGMT_POINT_TYPE_DNS_ONLY, CLUSTER_MGMT_POINT_TYPE_NONE, clusapi/CLUSTER_MGMT_POINT_TYPE, clusapi/CLUSTER_MGMT_POINT_TYPE_CNO, clusapi/CLUSTER_MGMT_POINT_TYPE_CNO_ONLY, clusapi/CLUSTER_MGMT_POINT_TYPE_DNS_ONLY, clusapi/CLUSTER_MGMT_POINT_TYPE_NONE, msclus/CLUSTER_MGMT_POINT_TYPE, msclus/CLUSTER_MGMT_POINT_TYPE_CNO, msclus/CLUSTER_MGMT_POINT_TYPE_CNO_ONLY, msclus/CLUSTER_MGMT_POINT_TYPE_DNS_ONLY, msclus/CLUSTER_MGMT_POINT_TYPE_NONE, mscs.cluster_mgmt_point_type
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: CLUSTER_MGMT_POINT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_MGMT_POINT_TYPE
 - clusapi/CLUSTER_MGMT_POINT_TYPE
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
 - CLUSTER_MGMT_POINT_TYPE
---

# CLUSTER_MGMT_POINT_TYPE enumeration


## -description

Specifies the type of the management point for the cluster.

<b>CLUSTER_MGMT_POINT_TYPE</b> is used as a possible value in the <a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a> configuration structure.

## -enum-fields

### -field CLUSTER_MGMT_POINT_TYPE_NONE:0

The cluster has no management point.

### -field CLUSTER_MGMT_POINT_TYPE_CNO

The management point is a cluster name object.

### -field CLUSTER_MGMT_POINT_TYPE_DNS_ONLY

The management point is DNS only.

### -field CLUSTER_MGMT_POINT_TYPE_CNO_ONLY

The management point type is cluster name object (CNO) only.

<b>Windows Server 2012 R2:  </b>This value is not supported before Windows Server 2016.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_ip_entry">CLUSTER_IP_ENTRY</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
