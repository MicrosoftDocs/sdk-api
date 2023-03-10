---
UID: NS:clusapi._CLUSTER_SHARED_VOLUME_STATE_INFO_EX
title: CLUSTER_SHARED_VOLUME_STATE_INFO_EX (clusapi.h)
description: Represents information about the state of a Cluster Shared Volume (CSV). (CLUSTER_SHARED_VOLUME_STATE_INFO_EX)
helpviewer_keywords: ["*PCLUSTER_SHARED_VOLUME_STATE_INFO_EX","CLUSTER_SHARED_VOLUME_STATE_INFO_EX","CLUSTER_SHARED_VOLUME_STATE_INFO_EX structure [Failover Cluster]","PCLUSTER_SHARED_VOLUME_STATE_INFO_EX","PCLUSTER_SHARED_VOLUME_STATE_INFO_EX structure pointer [Failover Cluster]","RedirectedIOReasonBitLockerInitializing","RedirectedIOReasonFileSystemTiering","RedirectedIOReasonMax","RedirectedIOReasonReFs","RedirectedIOReasonUnsafeFileSystemFilter","RedirectedIOReasonUnsafeVolumeFilter","RedirectedIOReasonUserRequest","VolumeRedirectedIOReasonMax","VolumeRedirectedIOReasonNoDiskConnectivity","VolumeRedirectedIOReasonStorageSpaceNotAttached","VolumeRedirectedIOReasonVolumeReplicationEnabled","clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO_EX","clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO_EX","mscs.cluster_shared_volume_state_info_ex"]
old-location: mscs\cluster_shared_volume_state_info_ex.htm
tech.root: MsCS
ms.assetid: B0926E1A-CA39-44FE-989C-B8BDD86F9683
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, CLUSTER_SHARED_VOLUME_STATE_INFO_EX, CLUSTER_SHARED_VOLUME_STATE_INFO_EX structure [Failover Cluster], PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, PCLUSTER_SHARED_VOLUME_STATE_INFO_EX structure pointer [Failover Cluster], RedirectedIOReasonBitLockerInitializing, RedirectedIOReasonFileSystemTiering, RedirectedIOReasonMax, RedirectedIOReasonReFs, RedirectedIOReasonUnsafeFileSystemFilter, RedirectedIOReasonUnsafeVolumeFilter, RedirectedIOReasonUserRequest, VolumeRedirectedIOReasonMax, VolumeRedirectedIOReasonNoDiskConnectivity, VolumeRedirectedIOReasonStorageSpaceNotAttached, VolumeRedirectedIOReasonVolumeReplicationEnabled, clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO_EX, clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, mscs.cluster_shared_volume_state_info_ex'
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
req.typenames: CLUSTER_SHARED_VOLUME_STATE_INFO_EX, *PCLUSTER_SHARED_VOLUME_STATE_INFO_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_SHARED_VOLUME_STATE_INFO_EX
 - clusapi/_CLUSTER_SHARED_VOLUME_STATE_INFO_EX
 - PCLUSTER_SHARED_VOLUME_STATE_INFO_EX
 - clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO_EX
 - CLUSTER_SHARED_VOLUME_STATE_INFO_EX
 - clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO_EX
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - CLUSTER_SHARED_VOLUME_STATE_INFO_EX
---

# CLUSTER_SHARED_VOLUME_STATE_INFO_EX structure


## -description

Represents information about the state of a Cluster Shared Volume (CSV).

## -struct-fields

### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string ends in a terminating null character. The name that is provided can be either the cluster-assigned friendly name or the volume GUID path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".

### -field szNodeName

The node name of the node that hosts the CSV.

### -field VolumeState

A <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_shared_volume_state">CLUSTER_SHARED_VOLUME_STATE</a> enumeration value that specifies the state of the CSV.

### -field szVolumeFriendlyName

The friendly name of the CSV.

### -field RedirectedIOReason

A bitmask that  specifies more specific reasons for the values stated in the <i>VolumeRedirectedIOReason</i> parameter.


This member can contain one or more of the following values:





#### RedirectedIOReasonUserRequest (0x0000000000000001)

A user request to enable direct access mode.



#### RedirectedIOReasonUnsafeFileSystemFilter (0x0000000000000002)

The file system filter is unsafe.



#### RedirectedIOReasonUnsafeVolumeFilter (0x0000000000000004)

The volume filter is unsafe.



#### RedirectedIOReasonFileSystemTiering (0x0000000000000008)

Tiered storage is enabled.



#### RedirectedIOReasonBitLockerInitializing (0x0000000000000010)

BitLocker is initializing.



#### RedirectedIOReasonReFs (0x0000000000000020)

TBD

<b>Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:  </b>This member was added in Windows Server 2016.



#### RedirectedIOReasonMax (0x8000000000000000)

All reasons.

### -field VolumeRedirectedIOReason

A bitmask that  specifies the reasons that direct access mode is enabled on the CSV.


This member can contain one or more of the following values:





#### VolumeRedirectedIOReasonNoDiskConnectivity (0x0000000000000001)

There is no disk connectivity.



#### VolumeRedirectedIOReasonStorageSpaceNotAttached (0x0000000000000002)

The storage space is not attached.



#### VolumeRedirectedIOReasonVolumeReplicationEnabled (0x0000000000000004)

Replication is enabled on the volume.

<b>Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:  </b>This member was added in Windows Server 2016.



#### VolumeRedirectedIOReasonMax (0x8000000000000000)

All reasons.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_shared_volume_state_info">CLUSTER_SHARED_VOLUME_STATE_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
