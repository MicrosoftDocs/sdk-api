---
UID: NE:clusapi._CLUSTER_CSV_VOLUME_FAULT_STATE
title: CLUSTER_CSV_VOLUME_FAULT_STATE (clusapi.h)
description: Defines the various fault states for a cluster shared volume (CSV).
helpviewer_keywords: ["*PCLUSTER_CSV_VOLUME_FAULT_STATE","CLUSTER_CSV_VOLUME_FAULT_STATE","CLUSTER_CSV_VOLUME_FAULT_STATE enumeration [Failover Cluster]","PCLUSTER_CSV_VOLUME_FAULT_STATE","PCLUSTER_CSV_VOLUME_FAULT_STATE enumeration pointer [Failover Cluster]","VolumeStateDismounted","VolumeStateInMaintenance","VolumeStateNoAccess","VolumeStateNoDirectIO","VolumeStateNoFaults","clusapi/CLUSTER_CSV_VOLUME_FAULT_STATE","clusapi/PCLUSTER_CSV_VOLUME_FAULT_STATE","clusapi/VolumeStateDismounted","clusapi/VolumeStateInMaintenance","clusapi/VolumeStateNoAccess","clusapi/VolumeStateNoDirectIO","clusapi/VolumeStateNoFaults","mscs.cluster_csv_volume_fault_state"]
old-location: mscs\cluster_csv_volume_fault_state.htm
tech.root: MsCS
ms.assetid: D3F065E5-3304-4B4E-BD85-04CAC050B001
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_CSV_VOLUME_FAULT_STATE, CLUSTER_CSV_VOLUME_FAULT_STATE, CLUSTER_CSV_VOLUME_FAULT_STATE enumeration [Failover Cluster], PCLUSTER_CSV_VOLUME_FAULT_STATE, PCLUSTER_CSV_VOLUME_FAULT_STATE enumeration pointer [Failover Cluster], VolumeStateDismounted, VolumeStateInMaintenance, VolumeStateNoAccess, VolumeStateNoDirectIO, VolumeStateNoFaults, clusapi/CLUSTER_CSV_VOLUME_FAULT_STATE, clusapi/PCLUSTER_CSV_VOLUME_FAULT_STATE, clusapi/VolumeStateDismounted, clusapi/VolumeStateInMaintenance, clusapi/VolumeStateNoAccess, clusapi/VolumeStateNoDirectIO, clusapi/VolumeStateNoFaults, mscs.cluster_csv_volume_fault_state'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Enterprise, Windows Server 2008 R2 Datacenter
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
req.typenames: CLUSTER_CSV_VOLUME_FAULT_STATE, *PCLUSTER_CSV_VOLUME_FAULT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_CSV_VOLUME_FAULT_STATE
 - clusapi/_CLUSTER_CSV_VOLUME_FAULT_STATE
 - PCLUSTER_CSV_VOLUME_FAULT_STATE
 - clusapi/PCLUSTER_CSV_VOLUME_FAULT_STATE
 - CLUSTER_CSV_VOLUME_FAULT_STATE
 - clusapi/CLUSTER_CSV_VOLUME_FAULT_STATE
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
 - CLUSTER_CSV_VOLUME_FAULT_STATE
---

# CLUSTER_CSV_VOLUME_FAULT_STATE enumeration


## -description

Defines the various fault states for a cluster shared volume (CSV).

## -enum-fields

### -field VolumeStateNoFaults:0x00000000

The CSV has no faults.

### -field VolumeStateNoDirectIO:0x00000001

Direct I/O is disabled for the CSV.

### -field VolumeStateNoAccess:0x00000002

The CSV can not be accessed.

### -field VolumeStateInMaintenance:0x00000004

The CSV is in maintenance mode.

### -field VolumeStateDismounted:0x00000008

The CSV is dismounted.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-clus_csv_volume_info">CLUS_CSV_VOLUME_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
