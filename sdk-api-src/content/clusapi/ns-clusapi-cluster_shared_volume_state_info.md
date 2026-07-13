---
UID: NS:clusapi._CLUSTER_SHARED_VOLUME_STATE_INFO
title: CLUSTER_SHARED_VOLUME_STATE_INFO (clusapi.h)
description: Represents information about the state of a Cluster Shared Volume (CSV). (CLUSTER_SHARED_VOLUME_STATE_INFO)
helpviewer_keywords: ["*PCLUSTER_SHARED_VOLUME_STATE_INFO","CLUSTER_SHARED_VOLUME_STATE_INFO","CLUSTER_SHARED_VOLUME_STATE_INFO structure [Failover Cluster]","PCLUSTER_SHARED_VOLUME_STATE_INFO","PCLUSTER_SHARED_VOLUME_STATE_INFO structure pointer [Failover Cluster]","clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO","clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO","mscs.cluster_shared_volume_state_info"]
old-location: mscs\cluster_shared_volume_state_info.htm
tech.root: MsCS
ms.assetid: 0E0DEF0B-C755-4B34-90D8-56BFEFEF2525
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_SHARED_VOLUME_STATE_INFO, CLUSTER_SHARED_VOLUME_STATE_INFO, CLUSTER_SHARED_VOLUME_STATE_INFO structure [Failover Cluster], PCLUSTER_SHARED_VOLUME_STATE_INFO, PCLUSTER_SHARED_VOLUME_STATE_INFO structure pointer [Failover Cluster], clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO, clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO, mscs.cluster_shared_volume_state_info'
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
req.typenames: CLUSTER_SHARED_VOLUME_STATE_INFO, *PCLUSTER_SHARED_VOLUME_STATE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_SHARED_VOLUME_STATE_INFO
 - clusapi/_CLUSTER_SHARED_VOLUME_STATE_INFO
 - PCLUSTER_SHARED_VOLUME_STATE_INFO
 - clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO
 - CLUSTER_SHARED_VOLUME_STATE_INFO
 - clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO
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
 - CLUSTER_SHARED_VOLUME_STATE_INFO
---

# CLUSTER_SHARED_VOLUME_STATE_INFO structure


## -description

Represents information about the state of a Cluster Shared Volume (CSV).

## -struct-fields

### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string ends in a terminating null character. The name that is provided can be either the cluster-assigned friendly name or the volume GUID path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".

### -field szNodeName

The node name  of the node that hosts the CSV.

### -field VolumeState

A <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_shared_volume_state">CLUSTER_SHARED_VOLUME_STATE</a> enumeration value that specifies the state of the CSV.

## -see-also

<a href="/windows/win32/api/clusapi/ns-clusapi-cluster_shared_volume_state_info_ex">CLUSTER_SHARED_VOLUME_STATE_INFO_EX</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
