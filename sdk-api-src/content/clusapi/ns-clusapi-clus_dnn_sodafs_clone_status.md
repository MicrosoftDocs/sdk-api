---
UID: NS:clusapi.CLUS_DNN_SODAFS_CLONE_STATUS
title: CLUS_DNN_SODAFS_CLONE_STATUS (clusapi.h)
description: Represents the status of a Scale-Out File Server clone.
helpviewer_keywords: ["*PCLUS_DNN_SODAFS_CLONE_STATUS","CLUS_DNN_SODAFS_CLONE_STATUS","CLUS_DNN_SODAFS_CLONE_STATUS structure [Failover Cluster]","PCLUS_DNN_SODAFS_CLONE_STATUS","PCLUS_DNN_SODAFS_CLONE_STATUS structure pointer [Failover Cluster]","clusapi/CLUS_DNN_SODAFS_CLONE_STATUS","clusapi/PCLUS_DNN_SODAFS_CLONE_STATUS","mscs.clus_dnn_sodafs_clone_status"]
old-location: mscs\clus_dnn_sodafs_clone_status.htm
tech.root: MsCS
ms.assetid: 3FD9AC64-3A7D-44C8-8066-AC1E7FB415DB
ms.date: 12/05/2018
ms.keywords: '*PCLUS_DNN_SODAFS_CLONE_STATUS, CLUS_DNN_SODAFS_CLONE_STATUS, CLUS_DNN_SODAFS_CLONE_STATUS structure [Failover Cluster], PCLUS_DNN_SODAFS_CLONE_STATUS, PCLUS_DNN_SODAFS_CLONE_STATUS structure pointer [Failover Cluster], clusapi/CLUS_DNN_SODAFS_CLONE_STATUS, clusapi/PCLUS_DNN_SODAFS_CLONE_STATUS, mscs.clus_dnn_sodafs_clone_status'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
req.typenames: CLUS_DNN_SODAFS_CLONE_STATUS, *PCLUS_DNN_SODAFS_CLONE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_DNN_SODAFS_CLONE_STATUS
 - clusapi/CLUS_DNN_SODAFS_CLONE_STATUS
 - PCLUS_DNN_SODAFS_CLONE_STATUS
 - clusapi/PCLUS_DNN_SODAFS_CLONE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_DNN_SODAFS_CLONE_STATUS
---

# CLUS_DNN_SODAFS_CLONE_STATUS structure


## -description

Represents the status of a Scale-Out File Server clone.

## -struct-fields

### -field NodeId

The node ID of the clone.

### -field Status

A <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration value that specifies the status of the clone.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_dnn_leader_status">CLUS_DNN_LEADER_STATUS</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>