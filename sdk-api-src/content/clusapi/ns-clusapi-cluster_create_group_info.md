---
UID: NS:clusapi._CLUSTER_CREATE_GROUP_INFO
title: CLUSTER_CREATE_GROUP_INFO (clusapi.h)
description: CLUSTER_CREATE_GROUP_INFO allows the caller to provide additional properties when creating a new group.
helpviewer_keywords: ["*PCLUSTER_CREATE_GROUP_INFO","CLUSTER_CREATE_GROUP_INFO","CLUSTER_CREATE_GROUP_INFO structure [Failover Cluster]","PCLUSTER_CREATE_GROUP_INFO","PCLUSTER_CREATE_GROUP_INFO structure pointer [Failover Cluster]","_CLUSTER_CREATE_GROUP_INFO","_CLUSTER_CREATE_GROUP_INFO structure [Failover Cluster]","clusapi/CLUSTER_CREATE_GROUP_INFO","clusapi/PCLUSTER_CREATE_GROUP_INFO","clusapi/_CLUSTER_CREATE_GROUP_INFO","msclus/CLUSTER_CREATE_GROUP_INFO","msclus/PCLUSTER_CREATE_GROUP_INFO","msclus/_CLUSTER_CREATE_GROUP_INFO","mscs.cluster_create_group_info"]
old-location: mscs\cluster_create_group_info.htm
tech.root: MsCS
ms.assetid: DBF71DAA-B8F1-42BF-AC82-FAFA9ADE4C44
ms.date: 08/03/2022
ms.keywords: '*PCLUSTER_CREATE_GROUP_INFO, CLUSTER_CREATE_GROUP_INFO, CLUSTER_CREATE_GROUP_INFO structure [Failover Cluster], PCLUSTER_CREATE_GROUP_INFO, PCLUSTER_CREATE_GROUP_INFO structure pointer [Failover Cluster], _CLUSTER_CREATE_GROUP_INFO, _CLUSTER_CREATE_GROUP_INFO structure [Failover Cluster], clusapi/CLUSTER_CREATE_GROUP_INFO, clusapi/PCLUSTER_CREATE_GROUP_INFO, clusapi/_CLUSTER_CREATE_GROUP_INFO, msclus/CLUSTER_CREATE_GROUP_INFO, msclus/PCLUSTER_CREATE_GROUP_INFO, msclus/_CLUSTER_CREATE_GROUP_INFO, mscs.cluster_create_group_info'
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
req.typenames: CLUSTER_CREATE_GROUP_INFO, *PCLUSTER_CREATE_GROUP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_CREATE_GROUP_INFO
 - clusapi/_CLUSTER_CREATE_GROUP_INFO
 - PCLUSTER_CREATE_GROUP_INFO
 - clusapi/PCLUSTER_CREATE_GROUP_INFO
 - CLUSTER_CREATE_GROUP_INFO
 - clusapi/CLUSTER_CREATE_GROUP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MSClus.h
api_name:
 - CLUSTER_CREATE_GROUP_INFO
---

# CLUSTER_CREATE_GROUP_INFO structure


## -description

Allows the caller to provide additional properties when creating a new group.

## -struct-fields

### -field dwVersion

The version of the <b>CLUSTER_CREATE_GROUP_INFO</b>.  Currently this is set to (<b>CLUSTER_CREATE_GROUP_INFO_VERSION_1</b> (0x00000001).

### -field groupType

The type of the cluster group that will be created.

